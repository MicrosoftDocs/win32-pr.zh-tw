---
title: 觸發程式。已啟用屬性
description: 針對腳本，取得或設定布林值，指出是否已啟用觸發程式。
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Enabled 屬性工作排程器
- 已啟用屬性工作排程器，觸發程式物件
- 觸發物件工作排程器，已啟用屬性
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934136"
---
# <a name="triggerenabled-property"></a>觸發程式。已啟用屬性

針對腳本，取得或設定布林值，指出是否已啟用觸發程式。

## <a name="syntax"></a>Syntax


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>屬性值

如果觸發程式已啟用，則為 True;否則為 false。 預設值是 true。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，已啟用的屬性會使用工作排程器架構的 [**enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) 元素來指定。

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

 

 





