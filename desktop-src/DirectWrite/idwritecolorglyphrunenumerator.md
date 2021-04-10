---
title: IDWriteColorGlyphRunEnumerator 介面
description: 此介面可讓應用程式透過色彩圖像執行來列舉。
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- IDWriteColorGlyphRunEnumerator 介面直接寫入
- IDWriteColorGlyphRunEnumerator 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686092"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="42dd1-105">IDWriteColorGlyphRunEnumerator 介面</span><span class="sxs-lookup"><span data-stu-id="42dd1-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="42dd1-106">此介面可讓應用程式透過色彩圖像執行來列舉。</span><span class="sxs-lookup"><span data-stu-id="42dd1-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="42dd1-107">列舉值會將層級列舉為適當的圖層，以作為適當的分層。</span><span class="sxs-lookup"><span data-stu-id="42dd1-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="42dd1-108">成員</span><span class="sxs-lookup"><span data-stu-id="42dd1-108">Members</span></span>

<span data-ttu-id="42dd1-109">**IDWriteColorGlyphRunEnumerator** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="42dd1-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="42dd1-110">**IDWriteColorGlyphRunEnumerator** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42dd1-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="42dd1-111">方法</span><span class="sxs-lookup"><span data-stu-id="42dd1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="42dd1-112">方法</span><span class="sxs-lookup"><span data-stu-id="42dd1-112">Methods</span></span>

<span data-ttu-id="42dd1-113">**IDWriteColorGlyphRunEnumerator** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="42dd1-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="42dd1-114">方法</span><span class="sxs-lookup"><span data-stu-id="42dd1-114">Method</span></span>                                                                | <span data-ttu-id="42dd1-115">描述</span><span class="sxs-lookup"><span data-stu-id="42dd1-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="42dd1-116">**GetCurrentRun**</span><span class="sxs-lookup"><span data-stu-id="42dd1-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="42dd1-117">傳回列舉值目前的圖像執行。</span><span class="sxs-lookup"><span data-stu-id="42dd1-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="42dd1-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="42dd1-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="42dd1-119">移至列舉值中的下一個圖像執行。</span><span class="sxs-lookup"><span data-stu-id="42dd1-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="42dd1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="42dd1-120">Requirements</span></span>



| <span data-ttu-id="42dd1-121">需求</span><span class="sxs-lookup"><span data-stu-id="42dd1-121">Requirement</span></span> | <span data-ttu-id="42dd1-122">值</span><span class="sxs-lookup"><span data-stu-id="42dd1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42dd1-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42dd1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42dd1-124">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42dd1-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="42dd1-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42dd1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42dd1-126">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42dd1-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="42dd1-127">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="42dd1-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="42dd1-128">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42dd1-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="42dd1-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="42dd1-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="42dd1-130"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42dd1-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="42dd1-131">DLL</span><span class="sxs-lookup"><span data-stu-id="42dd1-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42dd1-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42dd1-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

