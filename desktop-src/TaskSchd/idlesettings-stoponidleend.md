---
title: IdleSettings. StopOnIdleEnd 屬性
description: 針對腳本，取得或設定布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- StopOnIdleEnd 屬性工作排程器
- StopOnIdleEnd 屬性工作排程器，IdleSettings 物件
- IdleSettings 物件工作排程器、StopOnIdleEnd 屬性
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843264"
---
# <a name="idlesettingsstoponidleend-property"></a>IdleSettings. StopOnIdleEnd 屬性

針對腳本，取得或設定布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。

## <a name="syntax"></a>Syntax


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>屬性值

布林值，指出如果閒置條件在工作完成之前結束，工作排程器將終止工作。

## <a name="remarks"></a>備註

讀取或寫入工作的 XML 時，此設定會在工作排程器架構的 [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) 元素中指定。

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





