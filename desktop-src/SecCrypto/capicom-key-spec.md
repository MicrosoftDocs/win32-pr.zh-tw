---
description: CAPICOM \_ 金鑰 \_ 規格列舉會定義金鑰規格。
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: 'CAPICOM_KEY_SPEC 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 211830b57d37240edf0df97524ef3865ebe600b33e814353f3a0d021b1b0d88c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772443"
---
# <a name="capicom_key_spec-enumeration"></a>CAPICOM \_ 金鑰 \_ 規格列舉

**CAPICOM \_ 金鑰 \_ 規格** 列舉會定義金鑰規格。

## <a name="members"></a>成員



| member                              | 描述                                                | 值 |
|-------------------------------------|------------------------------------------------------------|-------|
| **CAPICOM \_ 金鑰 \_ 規格 \_ KEYEXCHANGE** | 金鑰可用於加密和簽署。<br/> | 1     |
| **CAPICOM \_ 金鑰 \_ 規格簽章 \_**   | 金鑰只能用於簽署。<br/>           | 2     |



## <a name="remarks"></a>備註

下列方法和屬性會使用 **CAPICOM \_ 金鑰 \_ 規格** 列舉：

-   [**PrivateKey. KeySpec**](privatekey-keyspec.md) 屬性。
-   [**PrivateKey。 Open**](privatekey-open.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




