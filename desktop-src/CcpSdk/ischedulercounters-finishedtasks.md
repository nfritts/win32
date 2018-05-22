---
Description: 'Retrieves the number of tasks that have finished running successfully.'
audience: developer
author: 'REDMOND\\danlep'
manager: 'REDMOND\\timlt'
ms.assetid: '9fa72d67-f431-4bd4-ab9d-973fe092b5b6'
ms.prod: 'windows-server-dev'
ms.technology: 'compute-cluster-pack'
ms.tgt_platform: multiple
title: 'ISchedulerCounters::FinishedTasks property'
---

# ISchedulerCounters::FinishedTasks property

Retrieves the number of tasks that have finished running successfully.

This property is read-only.

## Syntax


```C++
HRESULT get_FinishedTasks(
  [out]�long *pFinishedTasks
);
```



## Property value

The number of tasks that have finished running successfully.

## Error codes

If the method succeeds, the return value is S\_OK. Otherwise, the return value is an error code.

## Requirements



|                         |                                                                                                        |
|-------------------------|--------------------------------------------------------------------------------------------------------|
| Product<br/>      | HPC Pack 2008 R2 Client Utilities, HPC Pack 2008 Client Utilities<br/>                           |
| Type library<br/> | <dl> <dt>Microsoft.Hpc.Scheduler.tlb</dt> </dl> |



## See also

<dl> <dt>

[**ISchedulerCounters**](ischedulercounters.md)
</dt> </dl>

�

�



