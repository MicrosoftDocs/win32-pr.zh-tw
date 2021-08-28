---
description: 指出要搜尋 Active Directory 憑證存放區的位置。
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: 'CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 52f205717f3ba361c2c15dafc6e53f6cef3cd9d41cbbbf2ed243c60a74c2ca62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879438"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置列舉

**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置** 列舉型別會指出要搜尋 Active Directory [*憑證存放區*](../secgloss/c-gly.md)的位置。

## <a name="members"></a>成員



| member                               | 描述                                  | 值 |
|--------------------------------------|----------------------------------------------|-------|
| **CAPICOM \_ 搜尋 \_ 任何**             | 搜尋所有可用的位置。<br/> | 0     |
| **CAPICOM \_ 搜尋 \_ 全域 \_ 編錄** | 只搜尋通用類別目錄。<br/> | 1     |
| **CAPICOM \_ 搜尋 \_ 預設 \_ 網域** | 只搜尋預設網域。<br/> | 2     |



## <a name="remarks"></a>備註

下列屬性會使用這個列舉型別：

-   [**設定。ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
