---
description: 定義要從憑證查詢的資訊。
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: 'CAPICOM_CERT_INFO_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 480238556fce0470c51f00c394dd8566160686561342ec91da2e136c44a43cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879418"
---
# <a name="capicom_cert_info_type-enumeration"></a>CAPICOM \_ CERT \_ 資訊 \_ 類型列舉

**CAPICOM \_ CERT \_ INFO \_ 類型** 列舉類型會定義要從憑證查詢的資訊。

## <a name="members"></a>成員



| member                                         | 描述                                                                                  | 值 |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ 簡單 \_ 名稱** | 傳回憑證主體的顯示名稱。<br/>                              | 0     |
| **CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ 簡單 \_ 名稱**  | 傳回憑證簽發者的顯示名稱。<br/>                        | 1     |
| **CAPICOM \_ 憑證 \_ 資訊 \_ 主體 \_ 電子郵件 \_ 名稱**  | 傳回憑證主體的電子郵件地址。<br/>                             | 2     |
| **CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ 電子郵件 \_ 名稱**   | 傳回憑證簽發者的電子郵件地址。<br/>                       | 3     |
| **CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ UPN**          | 傳回憑證主體的 UPN。 在 CAPICOM 2.0 中引進。<br/>            | 4     |
| **CAPICOM \_ CERT \_ 資訊 \_ 簽發者 \_ UPN**           | 傳回憑證簽發者的 UPN。 在 CAPICOM 2.0 中引進。<br/>      | 5     |
| **CAPICOM \_ CERT \_ 資訊 \_ 主體 \_ DNS \_ 名稱**    | 傳回憑證主體的 DNS 名稱。 在 CAPICOM 2.0 中引進。<br/>       | 6     |
| **CAPICOM \_ 憑證 \_ 資訊 \_ 簽發者 \_ DNS \_ 名稱**     | 傳回憑證簽發者的 DNS 名稱。 在 CAPICOM 2.0 中引進。<br/> | 7     |



## <a name="remarks"></a>備註

[**GetInfo**](certificate-getinfo.md)方法會使用 **CAPICOM 憑證 \_ \_ 資訊 \_ 類型** 列舉類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




