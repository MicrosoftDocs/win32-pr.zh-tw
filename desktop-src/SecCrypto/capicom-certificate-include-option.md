---
description: 定義要儲存鏈中的哪些憑證。
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: 'CAPICOM_CERTIFICATE_INCLUDE_OPTION 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997011"
---
# <a name="capicom_certificate_include_option-enumeration"></a>CAPICOM \_ 憑證 \_ 包含 \_ 選項列舉

**CAPICOM \_ 憑證 \_ 包含 \_ 選項** 列舉型別會定義要儲存鏈中的哪些憑證。 此列舉類型是在 CAPICOM 2.0 中引進。

## <a name="members"></a>成員



| member                                                 | 描述                                                                           | 值 |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈** | 將所有憑證儲存在鏈中，但根實體除外。<br/> | 0     |
| **CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**        | 儲存完整的憑證鏈。<br/>                                      | 1     |
| **\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**   | 只儲存終端實體憑證。<br/>                                     | 2     |



## <a name="remarks"></a>備註

[ **CAPICOM \_ 憑證 \_ 包含] \_ 選項** 列舉類型是由 [**CERTIFICATE. Save**](certificate-save.md) 方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




