---
title: IDWriteFontFallbackBuilder 介面
description: 可讓您建立 Unicode 字型回撥對應，並從這些對應中建立字型的物件。
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- IDWriteFontFallbackBuilder 介面直接寫入
- IDWriteFontFallbackBuilder 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934612"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="27bf1-105">IDWriteFontFallbackBuilder 介面</span><span class="sxs-lookup"><span data-stu-id="27bf1-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="27bf1-106">可讓您建立 Unicode 字型回撥對應，並從這些對應中建立字型的物件。</span><span class="sxs-lookup"><span data-stu-id="27bf1-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="27bf1-107">成員</span><span class="sxs-lookup"><span data-stu-id="27bf1-107">Members</span></span>

<span data-ttu-id="27bf1-108">**IDWriteFontFallbackBuilder** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="27bf1-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="27bf1-109">**IDWriteFontFallbackBuilder** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="27bf1-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="27bf1-110">方法</span><span class="sxs-lookup"><span data-stu-id="27bf1-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="27bf1-111">方法</span><span class="sxs-lookup"><span data-stu-id="27bf1-111">Methods</span></span>

<span data-ttu-id="27bf1-112">**IDWriteFontFallbackBuilder** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="27bf1-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="27bf1-113">方法</span><span class="sxs-lookup"><span data-stu-id="27bf1-113">Method</span></span>                                                                      | <span data-ttu-id="27bf1-114">描述</span><span class="sxs-lookup"><span data-stu-id="27bf1-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27bf1-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="27bf1-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="27bf1-116">將單一對應附加至清單。</span><span class="sxs-lookup"><span data-stu-id="27bf1-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="27bf1-117">針對每個額外的對應呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="27bf1-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="27bf1-118">**AddMappings**</span><span class="sxs-lookup"><span data-stu-id="27bf1-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="27bf1-119">從現有的字型回溯物件加入所有對應。</span><span class="sxs-lookup"><span data-stu-id="27bf1-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="27bf1-120">**CreateFontFallback**</span><span class="sxs-lookup"><span data-stu-id="27bf1-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="27bf1-121">從新增的對應建立已完成的 fallback 物件。</span><span class="sxs-lookup"><span data-stu-id="27bf1-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="27bf1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="27bf1-122">Requirements</span></span>



| <span data-ttu-id="27bf1-123">需求</span><span class="sxs-lookup"><span data-stu-id="27bf1-123">Requirement</span></span> | <span data-ttu-id="27bf1-124">值</span><span class="sxs-lookup"><span data-stu-id="27bf1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27bf1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27bf1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="27bf1-126">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bf1-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="27bf1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27bf1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="27bf1-128">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bf1-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="27bf1-129">支援的最小電話</span><span class="sxs-lookup"><span data-stu-id="27bf1-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="27bf1-130">Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27bf1-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="27bf1-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="27bf1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="27bf1-132"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="27bf1-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="27bf1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="27bf1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27bf1-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27bf1-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

