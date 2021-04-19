---
description: IMediaLocator 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中驗證檔案名。
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: 'IMediaLocator 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998378"
---
# <a name="imedialocator-interface"></a><span data-ttu-id="b6260-103">IMediaLocator 介面</span><span class="sxs-lookup"><span data-stu-id="b6260-103">IMediaLocator interface</span></span>

> [!Note]  
> <span data-ttu-id="b6260-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b6260-104">\[Deprecated.</span></span> <span data-ttu-id="b6260-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b6260-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b6260-106">`IMediaLocator`介面會提供方法，在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="b6260-106">The `IMediaLocator` interface provides methods for validating file names in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="b6260-107">使用這個介面可確保指定的檔案名和路徑對應至現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="b6260-107">Use this interface to ensure that a given file name and path correspond to an existing file.</span></span> <span data-ttu-id="b6260-108">這個介面也提供一種方式來搜尋其他位置的檔案，以及顯示 **開啟** 的對話方塊，讓使用者可以找到檔案。</span><span class="sxs-lookup"><span data-stu-id="b6260-108">This interface also provides a way to search for the file at other locations, and to display an **Open** dialog box so that the user can locate the file.</span></span>

<span data-ttu-id="b6260-109">媒體定位器會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="b6260-109">The media locator implements this interface.</span></span> <span data-ttu-id="b6260-110">時間軸和轉譯引擎也支援透過下列方法進行的檔案名驗證：</span><span class="sxs-lookup"><span data-stu-id="b6260-110">The timeline and the render engine also support file name validation through the following methods:</span></span>

-   <span data-ttu-id="b6260-111">[**IAMTimeline：： ValidateSourceNames**](iamtimeline-validatesourcenames.md)：在時間軸中驗證和更新檔案名。</span><span class="sxs-lookup"><span data-stu-id="b6260-111">[**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md): Validates and updates file names in the timeline.</span></span>
-   <span data-ttu-id="b6260-112">[**IRenderEngine：： SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)：指定轉譯引擎如何在轉譯時驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="b6260-112">[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): Specifies how the render engine validates file names at rendering time.</span></span>

<span data-ttu-id="b6260-113">DES 應用程式通常會呼叫這些方法，而不是直接建立媒體定位器的實例。</span><span class="sxs-lookup"><span data-stu-id="b6260-113">Typically, a DES application will call these methods rather than directly create an instance of the media locator.</span></span> <span data-ttu-id="b6260-114">如需詳細資訊，請參閱 [使用媒體定位器](using-the-media-locator.md)。</span><span class="sxs-lookup"><span data-stu-id="b6260-114">For more information, see [Using the Media Locator](using-the-media-locator.md).</span></span>

## <a name="members"></a><span data-ttu-id="b6260-115">成員</span><span class="sxs-lookup"><span data-stu-id="b6260-115">Members</span></span>

<span data-ttu-id="b6260-116">**IMediaLocator** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b6260-116">The **IMediaLocator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b6260-117">**IMediaLocator** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b6260-117">**IMediaLocator** also has these types of members:</span></span>

-   [<span data-ttu-id="b6260-118">方法</span><span class="sxs-lookup"><span data-stu-id="b6260-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b6260-119">方法</span><span class="sxs-lookup"><span data-stu-id="b6260-119">Methods</span></span>

<span data-ttu-id="b6260-120">**IMediaLocator** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b6260-120">The **IMediaLocator** interface has these methods.</span></span>



| <span data-ttu-id="b6260-121">方法</span><span class="sxs-lookup"><span data-stu-id="b6260-121">Method</span></span>                                                     | <span data-ttu-id="b6260-122">描述</span><span class="sxs-lookup"><span data-stu-id="b6260-122">Description</span></span>                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b6260-123">**AddFoundLocation**</span><span class="sxs-lookup"><span data-stu-id="b6260-123">**AddFoundLocation**</span></span>](imedialocator-addfoundlocation.md) | <span data-ttu-id="b6260-124">將目錄新增至目錄快取。</span><span class="sxs-lookup"><span data-stu-id="b6260-124">Adds a directory to the directory cache.</span></span><br/>                                |
| [<span data-ttu-id="b6260-125">**FindMediaFile**</span><span class="sxs-lookup"><span data-stu-id="b6260-125">**FindMediaFile**</span></span>](imedialocator-findmediafile.md)       | <span data-ttu-id="b6260-126">搜尋檔案，如果成功，則會抓取檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b6260-126">Searches for a file and, if successful, retrieves the path to the file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b6260-127">備註</span><span class="sxs-lookup"><span data-stu-id="b6260-127">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6260-128">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b6260-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b6260-129">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b6260-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b6260-130">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b6260-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6260-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6260-131">Requirements</span></span>



| <span data-ttu-id="b6260-132">需求</span><span class="sxs-lookup"><span data-stu-id="b6260-132">Requirement</span></span> | <span data-ttu-id="b6260-133">值</span><span class="sxs-lookup"><span data-stu-id="b6260-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6260-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b6260-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b6260-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6260-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b6260-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6260-136">Library</span></span><br/> | <dl> <span data-ttu-id="b6260-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6260-137"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
