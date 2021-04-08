---
title: 'Windows 事件收集器常數 (Evcoll .h) '
description: Windows 事件收集器 SDK 包含下列常數。
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685468"
---
# <a name="windows-event-collector-constants"></a>Windows 事件收集器常數

Windows 事件收集器 SDK 包含下列常數。

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ VARIANT \_ 類型 \_ 遮罩**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



用來從 [**EC \_ 變異**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)的 **type** 屬性中遮罩陣列位，以將變數值的型別解壓縮。


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ VARIANT \_ 類型 \_ 陣列**
</dt> <dd> <dl> <dt>

128 (0x80) 
</dt> <dt>



當您在 [**EC \_ 變異**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant)的 **Type** 屬性中設定此位時，變數會包含值陣列的指標，而不是值本身。


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC \_ 讀取 \_ 許可權**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



讀取存取控制許可權，允許從事件收集器讀取資訊。


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC \_ 寫入 \_ 許可權**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



寫入存取控制許可權，允許將資訊寫入事件收集器。


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ \_ 永遠開啟**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



開啟現有的訂用帳戶，或建立訂用帳戶（如果不存在的話）。 由 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 方法所使用。


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ 建立 \_ 新的**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



傳遞至 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函數的旗標，指定應建立新的訂用帳戶。


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ 開啟 \_ 現有的**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



傳遞至 [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) 函數的旗標，指定應開啟現有的訂閱。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Evcoll。h</dt> </dl> |



 

 





