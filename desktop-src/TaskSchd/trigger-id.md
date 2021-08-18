---
title: Trigger.Id 屬性
description: 針對腳本，取得或設定觸發程式的識別碼。
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Id 屬性工作排程器
- Id 屬性工作排程器，觸發程式物件
- 觸發程式物件工作排程器，識別碼屬性
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c9ff851eab7b5e9cfb124bf03c83986d24b391d5ea109865ff2d59e2e33536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002156"
---
# <a name="triggerid-property"></a>Trigger.Id 屬性

針對腳本，取得或設定觸發程式的識別碼。

## <a name="syntax"></a>Syntax


```VB
Trigger.Id As String
```



## <a name="property-value"></a>屬性值

觸發程式的識別碼。 工作排程器使用此識別碼來進行記錄。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，會在個別觸發程式專案的 Id 屬性中指定觸發程式識別碼 (例如，工作排程器架構之 [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) 元素) 的 id 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





