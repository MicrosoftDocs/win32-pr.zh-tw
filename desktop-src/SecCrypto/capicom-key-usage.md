---
description: CAPICOM \_ 金鑰 \_ 使用方法列舉會定義金鑰的使用方式。 在 CAPICOM 2.0 中引進。
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: 'CAPICOM_KEY_USAGE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bb477ee12b33c3d32fd2c48a56831dc2f56244b1e8a564cd2d0482e6e4a5d5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772423"
---
# <a name="capicom_key_usage-enumeration"></a>CAPICOM \_ 金鑰 \_ 使用方法列舉

**CAPICOM \_ 金鑰 \_ 使用** 方法列舉會定義金鑰的使用方式。 在 CAPICOM 2.0 中引進。

## <a name="members"></a>成員



| member                                      | 描述                                                                                                                      | 值      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ 數位 \_ 簽名 \_ 金鑰 \_ 使用方式** | 金鑰可以用來建立數位簽章。<br/>                                                                    | 0x00000080 |
| **CAPICOM \_ 不可 \_ 否認性 \_ 金鑰 \_ 使用方法**   | 金鑰可用於不可 [*否認*](../secgloss/n-gly.md)性。<br/> | 0x00000040 |
| **CAPICOM \_ 金鑰 \_ 加密 \_ 金鑰 \_ 使用方法**  | 金鑰可以用來加密金鑰。<br/>                                                                                 | 0x00000020 |
| **CAPICOM \_ 資料 \_ 加密 \_ 金鑰 \_ 使用方法** | 金鑰可以用來加密資料。<br/>                                                                                  | 0x00000010 |
| **CAPICOM \_ 金鑰 \_ 合約 \_ 金鑰 \_ 使用方法**     | 金鑰可用於金鑰協定。<br/>                                                                                | 0x00000008 |
| **CAPICOM \_ 金鑰 \_ 憑證 \_ 簽署 \_ 金鑰 \_ 使用方法**    | 金鑰可用於金鑰憑證簽署。 此值相當於 CAPICOM \_ 離線 \_ CRL \_ 簽署 \_ 金鑰使用方式 \_ 。<br/> | 0x00000004 |
| **CAPICOM \_ 離線 \_ CRL \_ 簽署 \_ 金鑰 \_ 使用方法** | 金鑰可用於金鑰憑證簽署。 此值相當於 CAPICOM \_ 金鑰憑證 \_ \_ 簽署 \_ 金鑰使用方式 \_ 。<br/>    | 0x00000002 |
| **CAPICOM \_ CRL \_ 簽署 \_ 金鑰 \_ 使用方法**          | 金鑰可以用來簽署。<br/>                                                                                      | 0x00000002 |
| **CAPICOM \_ \_ 只加密 \_ 金鑰 \_ 使用方式**     | 金鑰只能用來加密。<br/>                                                                                  | 0x00000001 |
| **CAPICOM \_ \_ 只解密 \_ 金鑰 \_ 使用方式**     | 金鑰只能用來解密。<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
