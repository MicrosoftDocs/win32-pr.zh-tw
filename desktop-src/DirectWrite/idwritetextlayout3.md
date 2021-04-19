---
title: IDWriteTextLayout3 介面
description: 表示經過完整分析和格式化之後的一段文字。 |IDWriteTextLayout3 介面
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- IDWriteTextLayout3 介面直接寫入
- IDWriteTextLayout3 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986481"
---
# <a name="idwritetextlayout3-interface"></a><span data-ttu-id="d53d7-106">IDWriteTextLayout3 介面</span><span class="sxs-lookup"><span data-stu-id="d53d7-106">IDWriteTextLayout3 interface</span></span>

<span data-ttu-id="d53d7-107">表示經過完整分析和格式化之後的一段文字。</span><span class="sxs-lookup"><span data-stu-id="d53d7-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="d53d7-108">成員</span><span class="sxs-lookup"><span data-stu-id="d53d7-108">Members</span></span>

<span data-ttu-id="d53d7-109">**IDWriteTextLayout3** 介面繼承自 [**IDWriteTextLayout2**](idwritetextlayout2.md)。</span><span class="sxs-lookup"><span data-stu-id="d53d7-109">The **IDWriteTextLayout3** interface inherits from [**IDWriteTextLayout2**](idwritetextlayout2.md).</span></span> <span data-ttu-id="d53d7-110">**IDWriteTextLayout3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d53d7-110">**IDWriteTextLayout3** also has these types of members:</span></span>

-   [<span data-ttu-id="d53d7-111">方法</span><span class="sxs-lookup"><span data-stu-id="d53d7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d53d7-112">方法</span><span class="sxs-lookup"><span data-stu-id="d53d7-112">Methods</span></span>

<span data-ttu-id="d53d7-113">**IDWriteTextLayout3** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d53d7-113">The **IDWriteTextLayout3** interface has these methods.</span></span>



| <span data-ttu-id="d53d7-114">方法</span><span class="sxs-lookup"><span data-stu-id="d53d7-114">Method</span></span>                                                          | <span data-ttu-id="d53d7-115">描述</span><span class="sxs-lookup"><span data-stu-id="d53d7-115">Description</span></span>                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d53d7-116">**GetLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="d53d7-116">**GetLineMetrics**</span></span>](idwritetextlayout3-getlinemetrics.md)     | <span data-ttu-id="d53d7-117">抓取每一行的屬性。</span><span class="sxs-lookup"><span data-stu-id="d53d7-117">Retrieves properties of each line.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="d53d7-118">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="d53d7-118">**GetLineSpacing**</span></span>](idwritetextlayout3-getlinespacing.md)     | <span data-ttu-id="d53d7-119">取得行距資訊。</span><span class="sxs-lookup"><span data-stu-id="d53d7-119">Gets line spacing information.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="d53d7-120">**InvalidateLayout**</span><span class="sxs-lookup"><span data-stu-id="d53d7-120">**InvalidateLayout**</span></span>](idwritetextlayout3-invalidatelayout.md) | <span data-ttu-id="d53d7-121">使版面配置失效，並在呼叫度量或繪圖函式之前強制重新測量配置。</span><span class="sxs-lookup"><span data-stu-id="d53d7-121">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="d53d7-122">如果字型的位置變更、配置應重新繪製，或如果用戶端的大小已實 IDWriteInlineObject 變更，這項功能就很有用。</span><span class="sxs-lookup"><span data-stu-id="d53d7-122">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span> <br/> |
| [<span data-ttu-id="d53d7-123">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="d53d7-123">**SetLineSpacing**</span></span>](idwritetextlayout3-setlinespacing.md)     | <span data-ttu-id="d53d7-124">設定行間距。</span><span class="sxs-lookup"><span data-stu-id="d53d7-124">Set line spacing.</span></span><br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="d53d7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="d53d7-125">Requirements</span></span>



| <span data-ttu-id="d53d7-126">需求</span><span class="sxs-lookup"><span data-stu-id="d53d7-126">Requirement</span></span> | <span data-ttu-id="d53d7-127">值</span><span class="sxs-lookup"><span data-stu-id="d53d7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d53d7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d53d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d53d7-129">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d53d7-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d53d7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d53d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d53d7-131">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d53d7-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d53d7-132">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="d53d7-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d53d7-133">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d53d7-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d53d7-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="d53d7-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d53d7-135"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d53d7-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d53d7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d53d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d53d7-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d53d7-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d53d7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d53d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d53d7-139">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="d53d7-139">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





