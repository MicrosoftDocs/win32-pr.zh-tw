---
description: 根據可用的位置定義擴充金鑰使用方式名稱。
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: 'CAPICOM_EKU 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 365721c1378c4c0231b00dcf34ab32490d5006ed3bfd8e6dc585a90b9ac8b916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879358"
---
# <a name="capicom_eku-enumeration"></a>CAPICOM \_ EKU 列舉

**CAPICOM \_ EKU** 列舉型別會根據可用的位置來定義擴充金鑰使用方式名稱。

## <a name="members"></a>成員



| member                                     | 描述                                                                                                                                                 | 值 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ EKU \_ 其他**                    | 憑證具有在本機原則中定義的使用方式。 如果需要的 EKU 未預先定義，而且應用程式必須設定 OID 值，就會使用這個方法。<br/> | 0     |
| **CAPICOM \_ EKU \_ 伺服器 \_ 驗證**             | 憑證可以用來驗證服務器。<br/>                                                                                                | 1     |
| **CAPICOM \_ EKU \_ 用戶端 \_ 驗證**             | 憑證可以用來驗證用戶端。<br/>                                                                                                | 2     |
| **CAPICOM \_ EKU 程式 \_ 代碼 \_ 簽署**            | 憑證可以用來建立數位簽章。<br/>                                                                                           | 3     |
| **CAPICOM \_ EKU \_ 電子郵件 \_ 保護**        | 憑證可用於電子郵件保護。<br/>                                                                                                    | 4     |
| **CAPICOM \_ EKU \_ 智慧卡 \_ 登入**         | 憑證可用於智慧卡登入。 在 CAPICOM 2.0 中引進。<br/>                                                                         | 5     |
| **CAPICOM \_ EKU \_ 加密 \_ 檔 \_ 系統** | 憑證可用於 EFS。 在 CAPICOM 2.0 中引進。<br/>                                                                                      | 6     |



## <a name="remarks"></a>備註

Eku 會使用 **CAPICOM \_ eku** 列舉型別 [**。Name**](eku-name.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




