---
title: 'MrmPackagingOptions 列舉 (MrmResourceIndexer) '
description: 定義常數，指定 MrmCreateResourceFile 和 MrmCreateResourceFileInMemory 所建立之 PRI 檔案的選項。
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- MrmPackagingOptions 列舉功能表和其他資源
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965278"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="6c062-104">MrmPackagingOptions 列舉</span><span class="sxs-lookup"><span data-stu-id="6c062-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="6c062-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="6c062-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6c062-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="6c062-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6c062-107">定義常數，指定 [**MrmCreateResourceFile**](mrmcreateresourcefile.md) 和 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)所建立之 PRI 檔案的選項。</span><span class="sxs-lookup"><span data-stu-id="6c062-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="6c062-108">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="6c062-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c062-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c062-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="6c062-110">常數</span><span class="sxs-lookup"><span data-stu-id="6c062-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6c062-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span><span class="sxs-lookup"><span data-stu-id="6c062-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="6c062-112">未指定封裝選項。</span><span class="sxs-lookup"><span data-stu-id="6c062-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="6c062-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span><span class="sxs-lookup"><span data-stu-id="6c062-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="6c062-114">指定應建立無架構的資源套件。</span><span class="sxs-lookup"><span data-stu-id="6c062-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="6c062-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span><span class="sxs-lookup"><span data-stu-id="6c062-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="6c062-116">指定 PRI 檔案應該由所有支援的限定詞自動分割 (具體而言，就是語言和小數位數) 。</span><span class="sxs-lookup"><span data-stu-id="6c062-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c062-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c062-117">Requirements</span></span>



| <span data-ttu-id="6c062-118">需求</span><span class="sxs-lookup"><span data-stu-id="6c062-118">Requirement</span></span> | <span data-ttu-id="6c062-119">值</span><span class="sxs-lookup"><span data-stu-id="6c062-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c062-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c062-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c062-121">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c062-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6c062-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c062-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c062-123">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c062-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c062-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6c062-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c062-125"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c062-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c062-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c062-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c062-127">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="6c062-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

