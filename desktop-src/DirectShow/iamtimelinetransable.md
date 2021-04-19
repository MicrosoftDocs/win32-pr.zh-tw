---
description: IAMTimelineTransable 介面會將轉換新增至 DirectShow 編輯服務 (DES) 中的物件。
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: 'IAMTimelineTransable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999518"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="03ad5-103">IAMTimelineTransable 介面</span><span class="sxs-lookup"><span data-stu-id="03ad5-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="03ad5-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="03ad5-104">\[Deprecated.</span></span> <span data-ttu-id="03ad5-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="03ad5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="03ad5-106">`IAMTimelineTransable`介面會將轉換新增至[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的物件。</span><span class="sxs-lookup"><span data-stu-id="03ad5-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="03ad5-107">這個介面是由任何可以套用轉換的物件所公開，包括追蹤、組合和群組。</span><span class="sxs-lookup"><span data-stu-id="03ad5-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="03ad5-108">執行這個介面的物件可以有任意數目的轉換，但轉換不能以時間重迭。</span><span class="sxs-lookup"><span data-stu-id="03ad5-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="03ad5-109">音訊不支援轉換。</span><span class="sxs-lookup"><span data-stu-id="03ad5-109">Audio does not support transitions.</span></span> <span data-ttu-id="03ad5-110">音訊群組內的物件可以公開 `IAMTimelineTransable` 介面，但應用程式不應該將轉換新增至其中。</span><span class="sxs-lookup"><span data-stu-id="03ad5-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="03ad5-111">成員</span><span class="sxs-lookup"><span data-stu-id="03ad5-111">Members</span></span>

<span data-ttu-id="03ad5-112">**IAMTimelineTransable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="03ad5-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="03ad5-113">**IAMTimelineTransable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="03ad5-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="03ad5-114">方法</span><span class="sxs-lookup"><span data-stu-id="03ad5-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="03ad5-115">方法</span><span class="sxs-lookup"><span data-stu-id="03ad5-115">Methods</span></span>

<span data-ttu-id="03ad5-116">**IAMTimelineTransable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="03ad5-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="03ad5-117">方法</span><span class="sxs-lookup"><span data-stu-id="03ad5-117">Method</span></span>                                                          | <span data-ttu-id="03ad5-118">描述</span><span class="sxs-lookup"><span data-stu-id="03ad5-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03ad5-119">**GetNextTrans**</span><span class="sxs-lookup"><span data-stu-id="03ad5-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="03ad5-120">抓取在指定時間或之後出現的第一個轉換。</span><span class="sxs-lookup"><span data-stu-id="03ad5-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="03ad5-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="03ad5-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="03ad5-122">使用指定的時間做為 **REFTIME** 值，抓取在指定時間或之後出現的第一個轉換。</span><span class="sxs-lookup"><span data-stu-id="03ad5-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="03ad5-123">**GetTransAtTime**</span><span class="sxs-lookup"><span data-stu-id="03ad5-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="03ad5-124">抓取最接近指定時間的轉換。</span><span class="sxs-lookup"><span data-stu-id="03ad5-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="03ad5-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="03ad5-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="03ad5-126">在指定為 **REFTIME** 值的情況下，抓取最接近指定時間的轉換。</span><span class="sxs-lookup"><span data-stu-id="03ad5-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="03ad5-127">**TransAdd**</span><span class="sxs-lookup"><span data-stu-id="03ad5-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="03ad5-128">將轉換新增至物件。</span><span class="sxs-lookup"><span data-stu-id="03ad5-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="03ad5-129">**TransGetCount**</span><span class="sxs-lookup"><span data-stu-id="03ad5-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="03ad5-130">捕獲此物件的轉換數目。</span><span class="sxs-lookup"><span data-stu-id="03ad5-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="03ad5-131">備註</span><span class="sxs-lookup"><span data-stu-id="03ad5-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="03ad5-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="03ad5-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="03ad5-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="03ad5-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="03ad5-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="03ad5-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03ad5-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="03ad5-135">Requirements</span></span>



| <span data-ttu-id="03ad5-136">需求</span><span class="sxs-lookup"><span data-stu-id="03ad5-136">Requirement</span></span> | <span data-ttu-id="03ad5-137">值</span><span class="sxs-lookup"><span data-stu-id="03ad5-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03ad5-138">標頭</span><span class="sxs-lookup"><span data-stu-id="03ad5-138">Header</span></span><br/>  | <dl> <span data-ttu-id="03ad5-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="03ad5-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="03ad5-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="03ad5-140">Library</span></span><br/> | <dl> <span data-ttu-id="03ad5-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="03ad5-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
