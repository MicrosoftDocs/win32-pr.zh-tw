---
description: IRenderEngine2 介面可讓應用程式取代 (DES) 的 DirectShow 編輯服務所使用的預設影片調整大小篩選。 基本轉譯引擎和智慧型轉譯引擎都支援此介面。
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: 'IRenderEngine2 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991215"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="d5d40-104">IRenderEngine2 介面</span><span class="sxs-lookup"><span data-stu-id="d5d40-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="d5d40-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d5d40-105">\[Deprecated.</span></span> <span data-ttu-id="d5d40-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d5d40-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d5d40-107">`IRenderEngine2`介面可讓應用程式取代 (DES) 的 DirectShow 編輯服務所使用的預設影片調整大小篩選。</span><span class="sxs-lookup"><span data-stu-id="d5d40-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="d5d40-108">[基本轉譯引擎](basic-render-engine.md)和智慧型轉譯[引擎](smart-render-engine.md)都支援此介面。</span><span class="sxs-lookup"><span data-stu-id="d5d40-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="d5d40-109">成員</span><span class="sxs-lookup"><span data-stu-id="d5d40-109">Members</span></span>

<span data-ttu-id="d5d40-110">**IRenderEngine2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d5d40-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5d40-111">**IRenderEngine2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d5d40-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="d5d40-112">方法</span><span class="sxs-lookup"><span data-stu-id="d5d40-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5d40-113">方法</span><span class="sxs-lookup"><span data-stu-id="d5d40-113">Methods</span></span>

<span data-ttu-id="d5d40-114">**IRenderEngine2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d5d40-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="d5d40-115">方法</span><span class="sxs-lookup"><span data-stu-id="d5d40-115">Method</span></span>                                                  | <span data-ttu-id="d5d40-116">描述</span><span class="sxs-lookup"><span data-stu-id="d5d40-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5d40-117">**SetResizerGUID**</span><span class="sxs-lookup"><span data-stu-id="d5d40-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="d5d40-118">指定應用程式所提供之自訂調整大小篩選的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="d5d40-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5d40-119">備註</span><span class="sxs-lookup"><span data-stu-id="d5d40-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5d40-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d5d40-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d5d40-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d5d40-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d5d40-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d5d40-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d5d40-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5d40-123">Requirements</span></span>



| <span data-ttu-id="d5d40-124">需求</span><span class="sxs-lookup"><span data-stu-id="d5d40-124">Requirement</span></span> | <span data-ttu-id="d5d40-125">值</span><span class="sxs-lookup"><span data-stu-id="d5d40-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d40-126">版本</span><span class="sxs-lookup"><span data-stu-id="d5d40-126">Version</span></span><br/> | <span data-ttu-id="d5d40-127">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d5d40-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="d5d40-128">標頭</span><span class="sxs-lookup"><span data-stu-id="d5d40-128">Header</span></span><br/>  | <dl> <span data-ttu-id="d5d40-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d40-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d5d40-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5d40-130">Library</span></span><br/> | <dl> <span data-ttu-id="d5d40-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5d40-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d40-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5d40-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d40-133">提供自訂的影片調整</span><span class="sxs-lookup"><span data-stu-id="d5d40-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
