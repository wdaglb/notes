# camunda 工作流引擎

## 语义理解

- camunda 工作流平台引擎
- camunda modeler 流程模式设计器
- task 每个执行人的审批任务

## 步骤说明

启动流程并绑定 -> 审批流程 -> 监听事件完成自身对应的数据

## 启动流程

返回流程实例，将实例id存储起来，后续流程做识别用

```
this.runtimeService.startProcessInstanceById(flow.getTemplateId());
```

## 任务查询

查询一个指定实例id下某用户的任务，为空也就是没有权限审批

```
Task task = taskService.createTaskQuery()
    .taskAssignee("用户id")
    .processInstanceId("流程实例id")
    .singleResult();
```

## camunda admin

`http://localhost:8000/camunda/app/admin/default/`

## modeler

- 处理人只能为string，为long时会报异常
