---
title: RunningTask. InstanceGuid 屬性
description: 針對腳本，取得此工作實例的 GUID 識別碼。
ms.assetid: 35be538f-5223-4c61-9491-677953b4135a
keywords:
- InstanceGuid 屬性工作排程器
- InstanceGuid 屬性工作排程器，RunningTask 物件
- RunningTask 物件工作排程器、InstanceGuid 屬性
topic_type:
- apiref
api_name:
- RunningTask.InstanceGuid
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f3ad40eb7c8799d12ca3b4a6aaeb0b968a9229
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969613"
---
# <a name="runningtaskinstanceguid-property"></a>RunningTask. InstanceGuid 屬性

針對腳本，取得此工作實例的 GUID 識別碼。

## <a name="syntax"></a>Syntax


```VB
RunningTask.InstanceGuid As string
```



## <a name="property-value"></a>屬性值

此工作實例的 GUID 識別碼。 每次執行工作時，工作排程器服務都會產生一個識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





