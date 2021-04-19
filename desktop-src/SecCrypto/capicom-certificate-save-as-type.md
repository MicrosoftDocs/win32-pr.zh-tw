---
description: 定義包含憑證資訊之檔案的格式。
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: 'CAPICOM_CERTIFICATE_SAVE_AS_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989819"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_將 CAPICOM 憑證 \_ 儲存 \_ 為 \_ 類型列舉

[ **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** ] 列舉類型會定義包含憑證資訊之檔案的格式。 此列舉類型是由 CAPICOM 2.0 引進。

## <a name="members"></a>成員



| member                                  | 描述                                                                                                                                   | 值 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ PFX** | 輸出檔案將會格式化為 PFX (PKCS 12) 檔案，而且也會儲存任何可匯出的相關私密金鑰。<br/> | 0     |
| **\_將 CAPICOM 憑證 \_ 另存 \_ 為 \_ CER** | 輸出檔案將會格式化為 CER 檔案，且不會儲存任何私用金鑰。<br/>                                                        | 1     |



## <a name="remarks"></a>備註

[**憑證. save**](certificate-save.md)方法會使用 **CAPICOM \_ 憑證 \_ 儲存 \_ 為 \_ 類型** 列舉類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




