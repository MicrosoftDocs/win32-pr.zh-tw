---
description: 任何自訂的影片篩選器篩選器都必須支援 IResize 介面， (DES) 的 DirectShow 編輯服務。 若要設定自訂的調整器篩選，請在轉譯引擎上呼叫 IRenderEngine2：： SetResizerGUID 方法。
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: 'IResize 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000689"
---
# <a name="iresize-interface"></a><span data-ttu-id="7f056-104">IResize 介面</span><span class="sxs-lookup"><span data-stu-id="7f056-104">IResize interface</span></span>

> [!Note]  
> <span data-ttu-id="7f056-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7f056-105">\[Deprecated.</span></span> <span data-ttu-id="7f056-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7f056-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7f056-107">`IResize`任何自訂的視頻篩選器篩選器都必須支援此介面， (DES) 的 DirectShow 編輯服務。</span><span class="sxs-lookup"><span data-stu-id="7f056-107">The `IResize` interface must be supported by any custom video resizer filter for DirectShow Editing Services (DES).</span></span> <span data-ttu-id="7f056-108">若要設定自訂的調整器篩選，請在轉譯引擎上呼叫 [**IRenderEngine2：： SetResizerGUID**](irenderengine2-setresizerguid.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f056-108">To set a custom resizer filter, call the [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) method on the render engine.</span></span>

## <a name="members"></a><span data-ttu-id="7f056-109">成員</span><span class="sxs-lookup"><span data-stu-id="7f056-109">Members</span></span>

<span data-ttu-id="7f056-110">**IResize** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="7f056-110">The **IResize** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7f056-111">**IResize** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7f056-111">**IResize** also has these types of members:</span></span>

-   [<span data-ttu-id="7f056-112">方法</span><span class="sxs-lookup"><span data-stu-id="7f056-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7f056-113">方法</span><span class="sxs-lookup"><span data-stu-id="7f056-113">Methods</span></span>

<span data-ttu-id="7f056-114">**IResize** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7f056-114">The **IResize** interface has these methods.</span></span>



| <span data-ttu-id="7f056-115">方法</span><span class="sxs-lookup"><span data-stu-id="7f056-115">Method</span></span>                                          | <span data-ttu-id="7f056-116">描述</span><span class="sxs-lookup"><span data-stu-id="7f056-116">Description</span></span>                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="7f056-117">**取得 \_ InputSize**</span><span class="sxs-lookup"><span data-stu-id="7f056-117">**get\_InputSize**</span></span>](iresize-get-inputsize.md) | <span data-ttu-id="7f056-118">傳回檔整器篩選的目前輸入大小。</span><span class="sxs-lookup"><span data-stu-id="7f056-118">Returns the resizer filter's current input size.</span></span><br/>  |
| [<span data-ttu-id="7f056-119">**取得 \_ 媒體媒體**</span><span class="sxs-lookup"><span data-stu-id="7f056-119">**get\_MediaType**</span></span>](iresize-get-mediatype.md) | <span data-ttu-id="7f056-120">傳回檔整器篩選的輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7f056-120">Returns the resizer filter's output media type.</span></span><br/>   |
| [<span data-ttu-id="7f056-121">**取得 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7f056-121">**get\_Size**</span></span>](iresize-get-size.md)           | <span data-ttu-id="7f056-122">傳回目前的輸出大小和延展模式。</span><span class="sxs-lookup"><span data-stu-id="7f056-122">Returns the current output size and stretch mode.</span></span><br/> |
| [<span data-ttu-id="7f056-123">**put \_ 媒體存放**</span><span class="sxs-lookup"><span data-stu-id="7f056-123">**put\_MediaType**</span></span>](iresize-put-mediatype.md) | <span data-ttu-id="7f056-124">設定輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="7f056-124">Sets the output media type.</span></span><br/>                       |
| [<span data-ttu-id="7f056-125">**放置 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="7f056-125">**put\_Size**</span></span>](iresize-put-size.md)           | <span data-ttu-id="7f056-126">設定輸出大小和延展模式。</span><span class="sxs-lookup"><span data-stu-id="7f056-126">Sets the output size and stretch mode.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="7f056-127">備註</span><span class="sxs-lookup"><span data-stu-id="7f056-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7f056-128">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7f056-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7f056-129">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7f056-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7f056-130">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7f056-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7f056-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f056-131">Requirements</span></span>



| <span data-ttu-id="7f056-132">需求</span><span class="sxs-lookup"><span data-stu-id="7f056-132">Requirement</span></span> | <span data-ttu-id="7f056-133">值</span><span class="sxs-lookup"><span data-stu-id="7f056-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f056-134">版本</span><span class="sxs-lookup"><span data-stu-id="7f056-134">Version</span></span><br/> | <span data-ttu-id="7f056-135">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7f056-135">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="7f056-136">標頭</span><span class="sxs-lookup"><span data-stu-id="7f056-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7f056-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f056-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7f056-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="7f056-138">Library</span></span><br/> | <dl> <span data-ttu-id="7f056-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f056-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f056-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f056-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f056-141">提供自訂的影片調整</span><span class="sxs-lookup"><span data-stu-id="7f056-141">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
