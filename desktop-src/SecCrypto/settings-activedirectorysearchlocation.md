---
description: 設定或抓取 Active Directory 搜尋位置。
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: 設定。ActiveDirectorySearchLocation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 884866fd5ff6a3e3ff483a255bf2b77063ca81e51141108c9f58fd45629cc036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900318"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>設定。ActiveDirectorySearchLocation 屬性

\[**ActiveDirectorySearchLocation** 屬性可用於 [需求] 區段中指定的作業系統。\]

**ActiveDirectorySearchLocation** 屬性會設定或抓取 Active Directory 搜尋位置。

## <a name="syntax"></a>Syntax


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>屬性值

指定搜尋位置之 [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置**](capicom-active-directory-search-location.md) 列舉的值。 預設值是 [CAPICOM \_ 搜尋 \_ 任何]。 下表顯示可能的值。



| 值                                                                                                                                                                                                           | 意義                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ 搜尋 \_ 任何**</dt> </dl>                                   | 搜尋所有可用的位置。<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**CAPICOM \_ 搜尋 \_ 預設 \_ 網域**</dt> </dl> | 只搜尋預設網域。<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM \_ 搜尋 \_ 全域 \_ 編錄**</dt> </dl> | 只搜尋通用類別目錄。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**設定**](settings.md)
</dt> </dl>

 

 




