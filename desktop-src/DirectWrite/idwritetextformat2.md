---
title: IDWriteTextFormat2 介面
description: 描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。 |IDWriteTextFormat2 介面
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- IDWriteTextFormat2 介面直接寫入
- IDWriteTextFormat2 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992269"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="bb7c9-106">IDWriteTextFormat2 介面</span><span class="sxs-lookup"><span data-stu-id="bb7c9-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="bb7c9-107">描述用來格式化文字的字型和段落屬性，並說明地區設定資訊。</span><span class="sxs-lookup"><span data-stu-id="bb7c9-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="bb7c9-108">成員</span><span class="sxs-lookup"><span data-stu-id="bb7c9-108">Members</span></span>

<span data-ttu-id="bb7c9-109">**IDWriteTextFormat2** 介面繼承自 [**IDWriteTextFormat1**](idwritetextformat1.md)。</span><span class="sxs-lookup"><span data-stu-id="bb7c9-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="bb7c9-110">**IDWriteTextFormat2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bb7c9-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="bb7c9-111">方法</span><span class="sxs-lookup"><span data-stu-id="bb7c9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bb7c9-112">方法</span><span class="sxs-lookup"><span data-stu-id="bb7c9-112">Methods</span></span>

<span data-ttu-id="bb7c9-113">**IDWriteTextFormat2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bb7c9-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="bb7c9-114">方法</span><span class="sxs-lookup"><span data-stu-id="bb7c9-114">Method</span></span>                                                      | <span data-ttu-id="bb7c9-115">描述</span><span class="sxs-lookup"><span data-stu-id="bb7c9-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="bb7c9-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="bb7c9-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="bb7c9-117">取得多行文欄位落的行間距調整集。</span><span class="sxs-lookup"><span data-stu-id="bb7c9-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="bb7c9-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="bb7c9-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="bb7c9-119">設定行間距。</span><span class="sxs-lookup"><span data-stu-id="bb7c9-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="bb7c9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb7c9-120">Requirements</span></span>



| <span data-ttu-id="bb7c9-121">需求</span><span class="sxs-lookup"><span data-stu-id="bb7c9-121">Requirement</span></span> | <span data-ttu-id="bb7c9-122">值</span><span class="sxs-lookup"><span data-stu-id="bb7c9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7c9-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb7c9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bb7c9-124">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb7c9-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="bb7c9-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb7c9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bb7c9-126">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb7c9-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bb7c9-127">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="bb7c9-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bb7c9-128">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb7c9-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="bb7c9-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb7c9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb7c9-130"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb7c9-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bb7c9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bb7c9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb7c9-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb7c9-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb7c9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb7c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7c9-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="bb7c9-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

