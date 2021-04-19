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
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="428e2-103">CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置列舉</span><span class="sxs-lookup"><span data-stu-id="428e2-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="428e2-104">**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 搜尋 \_ 位置** 列舉型別會指出要搜尋 Active Directory [*憑證存放區*](../secgloss/c-gly.md)的位置。</span><span class="sxs-lookup"><span data-stu-id="428e2-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="428e2-105">成員</span><span class="sxs-lookup"><span data-stu-id="428e2-105">Members</span></span>



| <span data-ttu-id="428e2-106">member</span><span class="sxs-lookup"><span data-stu-id="428e2-106">Member</span></span>                               | <span data-ttu-id="428e2-107">描述</span><span class="sxs-lookup"><span data-stu-id="428e2-107">Description</span></span>                                  | <span data-ttu-id="428e2-108">值</span><span class="sxs-lookup"><span data-stu-id="428e2-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="428e2-109">**CAPICOM \_ 搜尋 \_ 任何**</span><span class="sxs-lookup"><span data-stu-id="428e2-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="428e2-110">搜尋所有可用的位置。</span><span class="sxs-lookup"><span data-stu-id="428e2-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="428e2-111">0</span><span class="sxs-lookup"><span data-stu-id="428e2-111">0</span></span>     |
| <span data-ttu-id="428e2-112">**CAPICOM \_ 搜尋 \_ 全域 \_ 編錄**</span><span class="sxs-lookup"><span data-stu-id="428e2-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="428e2-113">只搜尋通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="428e2-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="428e2-114">1</span><span class="sxs-lookup"><span data-stu-id="428e2-114">1</span></span>     |
| <span data-ttu-id="428e2-115">**CAPICOM \_ 搜尋 \_ 預設 \_ 網域**</span><span class="sxs-lookup"><span data-stu-id="428e2-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="428e2-116">只搜尋預設網域。</span><span class="sxs-lookup"><span data-stu-id="428e2-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="428e2-117">2</span><span class="sxs-lookup"><span data-stu-id="428e2-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="428e2-118">備註</span><span class="sxs-lookup"><span data-stu-id="428e2-118">Remarks</span></span>

<span data-ttu-id="428e2-119">下列屬性會使用這個列舉型別：</span><span class="sxs-lookup"><span data-stu-id="428e2-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="428e2-120">**設定. ActiveDirectorySearchLocation**</span><span class="sxs-lookup"><span data-stu-id="428e2-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="428e2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="428e2-121">Requirements</span></span>



| <span data-ttu-id="428e2-122">需求</span><span class="sxs-lookup"><span data-stu-id="428e2-122">Requirement</span></span> | <span data-ttu-id="428e2-123">值</span><span class="sxs-lookup"><span data-stu-id="428e2-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="428e2-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="428e2-124">Redistributable</span></span><br/> | <span data-ttu-id="428e2-125">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="428e2-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="428e2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="428e2-126">Header</span></span><br/>          | <dl> <span data-ttu-id="428e2-127"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="428e2-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
