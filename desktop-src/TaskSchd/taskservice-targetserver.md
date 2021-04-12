---
title: TaskService. TargetServer 屬性
description: 若為腳本，會取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- TargetServer 屬性工作排程器
- TargetServer 屬性工作排程器，TaskService 物件
- TaskService 物件工作排程器、TargetServer 屬性
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509436"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer 屬性

若為腳本，會取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。

## <a name="syntax"></a>Syntax


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>屬性值

正在執行使用者所連接之工作排程器服務的電腦名稱稱。

## <a name="remarks"></a>備註

當使用者傳遞 IP 位址、Localhost 或 '. ' 作為參數時，這個屬性會傳回空字串，而且當使用者未傳遞任何參數值時，它會傳回執行工作排程器服務的電腦名稱稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





