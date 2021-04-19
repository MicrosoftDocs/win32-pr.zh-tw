---
title: 'Windows 事件收集器資料類型 (Evcoll .h) '
description: Windows 事件收集器的資料類型會用來做為事件訂閱物件變數類型、函式參數類型和函式傳回類型。
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965272"
---
# <a name="windows-event-collector-data-types"></a>Windows 事件收集器資料類型

Windows 事件收集器的資料類型會用來做為事件訂閱物件變數類型、函式參數類型和函式傳回類型。


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**EC \_ 控制碼**
</dt> <dd>

訂用帳戶物件的控制碼。 用來表示事件收集器訂用帳戶。

</dd> <dt>

**EC \_ 物件 \_ 陣列 \_ 屬性 \_ 控制碼**
</dt> <dd>

訂用帳戶之事件來源的屬性值陣列控制碼。 當 **EcSubscriptionEventSources** 值傳遞至 *PropertyId* 參數時， [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)方法會傳回陣列控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Evcoll。h</dt> </dl> |



 

 





