---
title: 'MrmPackagingMode 列舉 (MrmResourceIndexer) '
description: 定義常數，指定 MrmCreateResourceFile 和 MrmCreateResourceFileInMemory 應該建立哪一種 PRI 檔 (s) 。
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- MrmPackagingMode 列舉功能表和其他資源
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317272"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="16eb2-104">MrmPackagingMode 列舉</span><span class="sxs-lookup"><span data-stu-id="16eb2-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="16eb2-105">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="16eb2-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="16eb2-106">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="16eb2-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="16eb2-107">定義常數，指定 [**MrmCreateResourceFile**](mrmcreateresourcefile.md) 和 [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)應該建立哪一種 PRI 檔 (s) 。</span><span class="sxs-lookup"><span data-stu-id="16eb2-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="16eb2-108">如需詳細資訊，以及如何使用這些 Api 的案例式逐步解說，請參閱 [封裝資源索引 (PRI) api 和自訂群組建系統](/windows/uwp/app-resources/pri-apis-custom-build-systems)。</span><span class="sxs-lookup"><span data-stu-id="16eb2-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="16eb2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="16eb2-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="16eb2-110">常數</span><span class="sxs-lookup"><span data-stu-id="16eb2-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="16eb2-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span><span class="sxs-lookup"><span data-stu-id="16eb2-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="16eb2-112">指定應建立單一 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="16eb2-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="16eb2-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span><span class="sxs-lookup"><span data-stu-id="16eb2-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="16eb2-114">指定應建立多個 PRI 檔案;由所有支援的限定詞自動分割 (具體而言，就是語言和小數位數) 。</span><span class="sxs-lookup"><span data-stu-id="16eb2-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="16eb2-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span><span class="sxs-lookup"><span data-stu-id="16eb2-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="16eb2-116">指定應建立附加元件附屬 PRI 檔案。</span><span class="sxs-lookup"><span data-stu-id="16eb2-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16eb2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="16eb2-117">Requirements</span></span>



| <span data-ttu-id="16eb2-118">需求</span><span class="sxs-lookup"><span data-stu-id="16eb2-118">Requirement</span></span> | <span data-ttu-id="16eb2-119">值</span><span class="sxs-lookup"><span data-stu-id="16eb2-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16eb2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16eb2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16eb2-121">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16eb2-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16eb2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16eb2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16eb2-123">\[僅限 Windows Server desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16eb2-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="16eb2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="16eb2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16eb2-125"><dt>MrmResourceIndexer。h</dt></span><span class="sxs-lookup"><span data-stu-id="16eb2-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16eb2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16eb2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16eb2-127">套件資源索引 (PRI) API 和自訂建置系統</span><span class="sxs-lookup"><span data-stu-id="16eb2-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

