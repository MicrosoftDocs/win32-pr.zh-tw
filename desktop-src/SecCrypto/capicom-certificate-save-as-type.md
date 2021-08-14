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
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772639"
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



 

 




