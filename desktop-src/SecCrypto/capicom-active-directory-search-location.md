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
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977165"
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

-   [**設定. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
