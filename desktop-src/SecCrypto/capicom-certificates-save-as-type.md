---
description: 定義包含憑證資訊之檔案的格式。
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: 'CAPICOM_CERTIFICATES_SAVE_AS_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879368"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ 類型列舉

[ **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** ] 列舉類型會定義包含憑證資訊之檔案的格式。 此列舉類型是由 CAPICOM 2.0 引進。

## <a name="members"></a>成員



| member                                          | 描述                                          | 值 |
|-------------------------------------------------|------------------------------------------------------|-------|
| **\_將 CAPICOM 憑證 \_ 另存為已 \_ \_ 序列化** | 已儲存的憑證會進行序列化。<br/>    | 0     |
| **\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PKCS7**      | 憑證會儲存為 PKCS \# 7。<br/> | 1     |
| **\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX**        | 憑證會儲存為 PFX。<br/>      | 2     |



## <a name="remarks"></a>備註

憑證所 \_ 使用的 CAPICOM 憑證 \_ 儲存 \_ 為 \_ 類型列舉類型。 [**儲存**](certificates-save.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




