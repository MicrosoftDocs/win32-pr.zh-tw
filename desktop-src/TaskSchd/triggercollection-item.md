---
title: TriggerCollection 專案屬性
description: 針對腳本，從集合取得指定的觸發程式。
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，TriggerCollection 物件
- TriggerCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685726"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection 專案屬性

針對腳本，從集合取得指定的觸發程式。

## <a name="syntax"></a>Syntax


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>屬性值

代表所要求之觸發程式的 [**觸發**](trigger.md) 程式物件。

## <a name="remarks"></a>備註

集合以1為基礎。 換句話說，集合中第一個專案的索引為1。

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

 

 





