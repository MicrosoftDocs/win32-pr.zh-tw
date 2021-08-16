---
description: 指出驗證數位簽章時要檢查的內容。
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: 'CAPICOM_SIGNED_DATA_VERIFY_FLAG 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8f087a9a28d06e63bc19d75974bccba05da4c77658f81401fd994a7eadb9726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772082"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>CAPICOM \_ 簽署的 \_ 資料 \_ 驗證旗標 \_ 列舉

**CAPICOM \_ 帶正負號 \_ 資料 \_ 驗證 \_ 旗** 標列舉指出驗證 [*數位簽章*](../secgloss/d-gly.md)時所檢查的內容。

## <a name="members"></a>成員



| member                                           | 描述                                                                                                 | 值 |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **\_ \_ 僅限 CAPICOM 驗證簽章 \_**             | 只會檢查簽章。<br/>                                                                   | 0     |
| **CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證** | 檢查簽章和用來建立簽章之憑證的有效性。<br/> | 1     |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
