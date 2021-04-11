---
title: DVD-ROM
description: 網域屬性會抓取 DVD 的目前網域。
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD-ROM Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317215"
---
# <a name="dvddomain"></a><span data-ttu-id="46d46-104">DVD-ROM</span><span class="sxs-lookup"><span data-stu-id="46d46-104">DVD.domain</span></span>

<span data-ttu-id="46d46-105">**網域** 屬性會抓取 DVD 的目前網域。</span><span class="sxs-lookup"><span data-stu-id="46d46-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="46d46-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="46d46-106">Possible Values</span></span>

<span data-ttu-id="46d46-107">這個屬性是唯讀 **字串** ，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="46d46-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="46d46-108">String</span><span class="sxs-lookup"><span data-stu-id="46d46-108">String</span></span>            | <span data-ttu-id="46d46-109">Description</span><span class="sxs-lookup"><span data-stu-id="46d46-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d46-110">firstPlay</span><span class="sxs-lookup"><span data-stu-id="46d46-110">firstPlay</span></span>         | <span data-ttu-id="46d46-111">執行 DVD 光碟的預設初始化。</span><span class="sxs-lookup"><span data-stu-id="46d46-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="46d46-112">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="46d46-112">videoManagerMenu</span></span>  | <span data-ttu-id="46d46-113">顯示整個光碟的功能表。也稱為 Windows Media Player 的 topMenu。</span><span class="sxs-lookup"><span data-stu-id="46d46-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="46d46-114">通常稱為標題功能表或頂端功能表。</span><span class="sxs-lookup"><span data-stu-id="46d46-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="46d46-115">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="46d46-115">videoTitleSetMenu</span></span> | <span data-ttu-id="46d46-116">顯示目前標題集的功能表。</span><span class="sxs-lookup"><span data-stu-id="46d46-116">Displaying menus for current title set.</span></span> <span data-ttu-id="46d46-117">也稱為 Windows Media Player 的 titleMenu。</span><span class="sxs-lookup"><span data-stu-id="46d46-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="46d46-118">通常稱為根功能表。</span><span class="sxs-lookup"><span data-stu-id="46d46-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="46d46-119">title</span><span class="sxs-lookup"><span data-stu-id="46d46-119">title</span></span>             | <span data-ttu-id="46d46-120">通常會顯示目前的標題。</span><span class="sxs-lookup"><span data-stu-id="46d46-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="46d46-121">stop</span><span class="sxs-lookup"><span data-stu-id="46d46-121">stop</span></span>              | <span data-ttu-id="46d46-122">DVD 導覽器位於 DVD 停止網域中。</span><span class="sxs-lookup"><span data-stu-id="46d46-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="46d46-123">未定義</span><span class="sxs-lookup"><span data-stu-id="46d46-123">undefined</span></span>         | <span data-ttu-id="46d46-124">播放程式不在任何 DVD 網域中。</span><span class="sxs-lookup"><span data-stu-id="46d46-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="46d46-125">備註</span><span class="sxs-lookup"><span data-stu-id="46d46-125">Remarks</span></span>

<span data-ttu-id="46d46-126">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="46d46-126">Every DVD is authored differently.</span></span> <span data-ttu-id="46d46-127">某些 Dvd 不包含 firstPlay、videoManagerMenu 或 videoTitleSetMenu 網域。</span><span class="sxs-lookup"><span data-stu-id="46d46-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="46d46-128">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="46d46-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d46-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d46-129">Requirements</span></span>



| <span data-ttu-id="46d46-130">需求</span><span class="sxs-lookup"><span data-stu-id="46d46-130">Requirement</span></span> | <span data-ttu-id="46d46-131">值</span><span class="sxs-lookup"><span data-stu-id="46d46-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46d46-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d46-132">Minimum supported client</span></span><br/> | <span data-ttu-id="46d46-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d46-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46d46-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d46-134">Minimum supported server</span></span><br/> | <span data-ttu-id="46d46-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d46-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46d46-136">版本</span><span class="sxs-lookup"><span data-stu-id="46d46-136">Version</span></span><br/>                  | <span data-ttu-id="46d46-137">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="46d46-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="46d46-138">DLL</span><span class="sxs-lookup"><span data-stu-id="46d46-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46d46-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46d46-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d46-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46d46-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d46-141">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="46d46-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





