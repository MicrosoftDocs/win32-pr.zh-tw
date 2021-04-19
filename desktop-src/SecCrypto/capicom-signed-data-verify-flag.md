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
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996422"
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



 

 
