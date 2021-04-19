---
description: 與 Store. Open 方法搭配使用，以指出如何開啟憑證存放區。
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: 'CAPICOM_STORE_OPEN_MODE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995402"
---
# <a name="capicom_store_open_mode-enumeration"></a>CAPICOM \_ 存放區 \_ 開啟 \_ 模式列舉

CAPICOM \_ 存放區 \_ 開啟 \_ 模式列舉型別會與 [**STORE. open**](store-open.md) 方法搭配使用，以指出如何開啟憑證存放區。

## <a name="members"></a>成員



| member                                      | 描述                                                                                                                                                              | 值 |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_**        | 在唯讀模式開啟存放區。<br/>                                                                                                                             | 0     |
| **CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫**       | 以讀取/寫入模式開啟存放區。<br/>                                                                                                                            | 1     |
| **允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_**  | 如果使用者具有讀取/寫入權限，請以讀取/寫入模式開啟存放區。 如果使用者沒有讀取/寫入權限，請在唯讀模式中開啟存放區。<br/> | 2     |
| **CAPICOM \_ 存放 \_ 區 \_ 僅開啟現有 \_ 的**    | 僅開啟現有的商店;請勿建立新的存放區。 由 CAPICOM 2.0 引進。<br/>                                                                              | 128   |
| **開啟的 CAPICOM \_ 存放區 \_ \_ 包含 \_ 封存** | 使用存放區時，請包含封存的憑證。 由 CAPICOM 2.0 引進。<br/>                                                                                | 256   |



## <a name="remarks"></a>備註

使用 CAPICOM \_ 存放區 \_ 開放式 \_ 模式列舉時，只能使用下列其中一個設定。

-   CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_
-   CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫
-   允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 




