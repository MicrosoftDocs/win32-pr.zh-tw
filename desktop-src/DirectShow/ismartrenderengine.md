---
description: ISmartRenderEngine 介面提供的方法，可支援 DirectShow 編輯服務中的智慧型 recompression (DES) 。 智慧型轉譯引擎會公開這個介面。
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: 'ISmartRenderEngine 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999211"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="165df-104">ISmartRenderEngine 介面</span><span class="sxs-lookup"><span data-stu-id="165df-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="165df-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="165df-105">\[Deprecated.</span></span> <span data-ttu-id="165df-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="165df-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="165df-107">`ISmartRenderEngine`介面提供的方法可支援[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的智慧型 recompression。</span><span class="sxs-lookup"><span data-stu-id="165df-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="165df-108">智慧型轉譯引擎會公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="165df-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="165df-109">成員</span><span class="sxs-lookup"><span data-stu-id="165df-109">Members</span></span>

<span data-ttu-id="165df-110">**ISmartRenderEngine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="165df-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="165df-111">**ISmartRenderEngine** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="165df-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="165df-112">方法</span><span class="sxs-lookup"><span data-stu-id="165df-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="165df-113">方法</span><span class="sxs-lookup"><span data-stu-id="165df-113">Methods</span></span>

<span data-ttu-id="165df-114">**ISmartRenderEngine** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="165df-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="165df-115">方法</span><span class="sxs-lookup"><span data-stu-id="165df-115">Method</span></span>                                                                | <span data-ttu-id="165df-116">描述</span><span class="sxs-lookup"><span data-stu-id="165df-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="165df-117">**GetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="165df-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="165df-118">抓取指定群組的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="165df-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="165df-119">**SetFindCompressorCB**</span><span class="sxs-lookup"><span data-stu-id="165df-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="165df-120">未實作。</span><span class="sxs-lookup"><span data-stu-id="165df-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="165df-121">**SetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="165df-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="165df-122">指定轉譯指定群組時要使用的壓縮篩選。</span><span class="sxs-lookup"><span data-stu-id="165df-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="165df-123">備註</span><span class="sxs-lookup"><span data-stu-id="165df-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="165df-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="165df-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="165df-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="165df-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="165df-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="165df-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="165df-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="165df-127">Requirements</span></span>



| <span data-ttu-id="165df-128">需求</span><span class="sxs-lookup"><span data-stu-id="165df-128">Requirement</span></span> | <span data-ttu-id="165df-129">值</span><span class="sxs-lookup"><span data-stu-id="165df-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="165df-130">標頭</span><span class="sxs-lookup"><span data-stu-id="165df-130">Header</span></span><br/>  | <dl> <span data-ttu-id="165df-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="165df-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="165df-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="165df-132">Library</span></span><br/> | <dl> <span data-ttu-id="165df-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="165df-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165df-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="165df-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165df-135">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="165df-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
