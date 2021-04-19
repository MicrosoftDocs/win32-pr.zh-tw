---
description: 設定或抓取 Active Directory 搜尋位置。
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: ActiveDirectorySearchLocation 屬性
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
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000856"
---
# <a name="settingsactivedirectorysearchlocation-property"></a><span data-ttu-id="4d2e3-103">ActiveDirectorySearchLocation 屬性</span><span class="sxs-lookup"><span data-stu-id="4d2e3-103">Settings.ActiveDirectorySearchLocation property</span></span>

<span data-ttu-id="4d2e3-104">\[**ActiveDirectorySearchLocation** 屬性可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="4d2e3-104">\[The **ActiveDirectorySearchLocation** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="4d2e3-105">**ActiveDirectorySearchLocation** 屬性會設定或抓取 Active Directory 搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-105">The **ActiveDirectorySearchLocation** property sets or retrieves the Active Directory search location.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d2e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d2e3-106">Syntax</span></span>


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="4d2e3-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="4d2e3-107">Property value</span></span>

<span data-ttu-id="4d2e3-108">指定搜尋位置之 [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置**](capicom-active-directory-search-location.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-108">A value of the [**CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION**](capicom-active-directory-search-location.md) enumeration that specifies the search location.</span></span> <span data-ttu-id="4d2e3-109">預設值是 [CAPICOM \_ 搜尋 \_ 任何]。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-109">The default value is CAPICOM\_SEARCH\_ANY.</span></span> <span data-ttu-id="4d2e3-110">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="4d2e3-111">值</span><span class="sxs-lookup"><span data-stu-id="4d2e3-111">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="4d2e3-112">意義</span><span class="sxs-lookup"><span data-stu-id="4d2e3-112">Meaning</span></span>                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <span data-ttu-id="4d2e3-113"><dt>**CAPICOM \_ 搜尋 \_ 任何**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e3-113"><dt>**CAPICOM\_SEARCH\_ANY**</dt></span></span> </dl>                                   | <span data-ttu-id="4d2e3-114">搜尋所有可用的位置。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-114">Search all available locations.</span></span><br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <span data-ttu-id="4d2e3-115"><dt>**CAPICOM \_ 搜尋 \_ 預設 \_ 網域**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e3-115"><dt>**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="4d2e3-116">只搜尋預設網域。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-116">Search only the default domain.</span></span><br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <span data-ttu-id="4d2e3-117"><dt>**CAPICOM \_ 搜尋 \_ 全域 \_ 編錄**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e3-117"><dt>**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</dt></span></span> </dl> | <span data-ttu-id="4d2e3-118">只搜尋通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="4d2e3-118">Search only the global catalog.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4d2e3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d2e3-119">Requirements</span></span>



| <span data-ttu-id="4d2e3-120">需求</span><span class="sxs-lookup"><span data-stu-id="4d2e3-120">Requirement</span></span> | <span data-ttu-id="4d2e3-121">值</span><span class="sxs-lookup"><span data-stu-id="4d2e3-121">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2e3-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4d2e3-122">Redistributable</span></span><br/> | <span data-ttu-id="4d2e3-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4d2e3-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4d2e3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2e3-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="4d2e3-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2e3-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2e3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d2e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2e3-127">**設定**</span><span class="sxs-lookup"><span data-stu-id="4d2e3-127">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




