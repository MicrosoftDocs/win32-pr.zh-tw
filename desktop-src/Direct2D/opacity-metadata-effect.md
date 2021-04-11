---
title: 不透明度中繼資料效果
description: 您可以使用此效果將輸入影像的區域標記為不透明，因此可能會對圖形進行內部呈現優化。
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105449"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="41333-103">不透明度中繼資料效果</span><span class="sxs-lookup"><span data-stu-id="41333-103">Opacity metadata effect</span></span>

<span data-ttu-id="41333-104">您可以使用此效果將輸入影像的區域標記為不透明，因此可能會對圖形進行內部呈現優化。</span><span class="sxs-lookup"><span data-stu-id="41333-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="41333-105">這種效果不會將影像本身修改為不透明。</span><span class="sxs-lookup"><span data-stu-id="41333-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="41333-106">它會修改與影像相關聯的資料，讓轉譯器假設指定的區域不透明。</span><span class="sxs-lookup"><span data-stu-id="41333-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="41333-107">這項效果的 CLSID 是 CLSID \_ D2D1OpacityMetadata。</span><span class="sxs-lookup"><span data-stu-id="41333-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="41333-108">效果屬性</span><span class="sxs-lookup"><span data-stu-id="41333-108">Effect properties</span></span>



| <span data-ttu-id="41333-109">顯示名稱和索引列舉</span><span class="sxs-lookup"><span data-stu-id="41333-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="41333-110">類型和預設值</span><span class="sxs-lookup"><span data-stu-id="41333-110">Type and default value</span></span>                                                             | <span data-ttu-id="41333-111">Description</span><span class="sxs-lookup"><span data-stu-id="41333-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41333-112">OutputRect</span><span class="sxs-lookup"><span data-stu-id="41333-112">OutputRect</span></span><br/> <span data-ttu-id="41333-113">D2D1 \_ OPACITYMETADATA 的 \_ 主張 \_ 輸入不透明的 \_ \_ RECT</span><span class="sxs-lookup"><span data-stu-id="41333-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="41333-114">D2D1 \_ 向量 \_ 4F</span><span class="sxs-lookup"><span data-stu-id="41333-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="41333-115"> (-FLT \_ max、-FLT \_ MAX、FLT \_ max、FLT \_ MAX) </span><span class="sxs-lookup"><span data-stu-id="41333-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="41333-116">來源影像中不透明的部分。</span><span class="sxs-lookup"><span data-stu-id="41333-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="41333-117">預設值是整個輸入影像。</span><span class="sxs-lookup"><span data-stu-id="41333-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41333-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="41333-118">Requirements</span></span>



| <span data-ttu-id="41333-119">需求</span><span class="sxs-lookup"><span data-stu-id="41333-119">Requirement</span></span> | <span data-ttu-id="41333-120">值</span><span class="sxs-lookup"><span data-stu-id="41333-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41333-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41333-121">Minimum supported client</span></span> | <span data-ttu-id="41333-122">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41333-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="41333-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41333-123">Minimum supported server</span></span> | <span data-ttu-id="41333-124">適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41333-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="41333-125">標頭</span><span class="sxs-lookup"><span data-stu-id="41333-125">Header</span></span>                   | <span data-ttu-id="41333-126">d2d1effects。h</span><span class="sxs-lookup"><span data-stu-id="41333-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="41333-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="41333-127">Library</span></span>                  | <span data-ttu-id="41333-128">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="41333-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="41333-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="41333-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41333-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="41333-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

