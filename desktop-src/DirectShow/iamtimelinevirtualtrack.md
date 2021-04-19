---
description: IAMTimelineVirtualTrack 介面提供在 DirectShow 編輯服務 (DES) 中使用虛擬追蹤的方法。 組合和追蹤支援此介面。
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: 'IAMTimelineVirtualTrack 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978687"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="06588-104">IAMTimelineVirtualTrack 介面</span><span class="sxs-lookup"><span data-stu-id="06588-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="06588-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="06588-105">\[Deprecated.</span></span> <span data-ttu-id="06588-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="06588-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="06588-107">`IAMTimelineVirtualTrack`介面提供在[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中使用虛擬追蹤的方法。</span><span class="sxs-lookup"><span data-stu-id="06588-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="06588-108">組合和追蹤支援此介面。</span><span class="sxs-lookup"><span data-stu-id="06588-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="06588-109">成員</span><span class="sxs-lookup"><span data-stu-id="06588-109">Members</span></span>

<span data-ttu-id="06588-110">**IAMTimelineVirtualTrack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="06588-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="06588-111">**IAMTimelineVirtualTrack** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06588-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="06588-112">方法</span><span class="sxs-lookup"><span data-stu-id="06588-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="06588-113">方法</span><span class="sxs-lookup"><span data-stu-id="06588-113">Methods</span></span>

<span data-ttu-id="06588-114">**IAMTimelineVirtualTrack** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06588-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="06588-115">方法</span><span class="sxs-lookup"><span data-stu-id="06588-115">Method</span></span>                                                               | <span data-ttu-id="06588-116">描述</span><span class="sxs-lookup"><span data-stu-id="06588-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="06588-117">**SetTrackDirty**</span><span class="sxs-lookup"><span data-stu-id="06588-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="06588-118">不支援。</span><span class="sxs-lookup"><span data-stu-id="06588-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="06588-119">**TrackGetPriority**</span><span class="sxs-lookup"><span data-stu-id="06588-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="06588-120">抓取物件的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="06588-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06588-121">備註</span><span class="sxs-lookup"><span data-stu-id="06588-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06588-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="06588-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="06588-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="06588-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="06588-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="06588-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06588-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="06588-125">Requirements</span></span>



| <span data-ttu-id="06588-126">需求</span><span class="sxs-lookup"><span data-stu-id="06588-126">Requirement</span></span> | <span data-ttu-id="06588-127">值</span><span class="sxs-lookup"><span data-stu-id="06588-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06588-128">標頭</span><span class="sxs-lookup"><span data-stu-id="06588-128">Header</span></span><br/>  | <dl> <span data-ttu-id="06588-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="06588-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="06588-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="06588-130">Library</span></span><br/> | <dl> <span data-ttu-id="06588-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="06588-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
