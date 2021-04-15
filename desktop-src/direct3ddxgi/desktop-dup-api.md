---
description: Windows 8 停用標準 Windows 2000 顯示驅動程式模型 (XDDM) 鏡像驅動程式，並改為提供桌面複製 API。
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: 桌面複製 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467531"
---
# <a name="desktop-duplication-api"></a><span data-ttu-id="e4fbe-103">桌面複製 API</span><span class="sxs-lookup"><span data-stu-id="e4fbe-103">Desktop Duplication API</span></span>

<span data-ttu-id="e4fbe-104">Windows 8 停用標準 Windows 2000 顯示驅動程式模型 (XDDM) 鏡像驅動程式，並改為提供桌面複製 API。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-104">Windows 8 disables standard Windows 2000 Display Driver Model (XDDM) mirror drivers and offers the desktop duplication API instead.</span></span> <span data-ttu-id="e4fbe-105">桌面複製 API 可讓您從遠端存取桌面映射以進行共同作業案例。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-105">The desktop duplication API provides remote access to a desktop image for collaboration scenarios.</span></span> <span data-ttu-id="e4fbe-106">應用程式可以使用桌面複製 API 來存取桌面的逐幀更新。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-106">Apps can use the desktop duplication API to access frame-by-frame updates to the desktop.</span></span> <span data-ttu-id="e4fbe-107">由於應用程式會在 DXGI 介面中接收桌面映射的更新，因此應用程式可以使用 GPU 的完整功能來處理映射更新。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-107">Because apps receive updates to the desktop image in a DXGI surface, the apps can use the full power of the GPU to process the image updates.</span></span>

-   [<span data-ttu-id="e4fbe-108">更新桌面映射資料</span><span class="sxs-lookup"><span data-stu-id="e4fbe-108">Updating the desktop image data</span></span>](#updating-the-desktop-image-data)
-   [<span data-ttu-id="e4fbe-109">旋轉桌面映射</span><span class="sxs-lookup"><span data-stu-id="e4fbe-109">Rotating the desktop image</span></span>](#rotating-the-desktop-image)
-   [<span data-ttu-id="e4fbe-110">更新桌面指標</span><span class="sxs-lookup"><span data-stu-id="e4fbe-110">Updating the desktop pointer</span></span>](#updating-the-desktop-pointer)
-   [<span data-ttu-id="e4fbe-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4fbe-111">Related topics</span></span>](#related-topics)

## <a name="updating-the-desktop-image-data"></a><span data-ttu-id="e4fbe-112">更新桌面映射資料</span><span class="sxs-lookup"><span data-stu-id="e4fbe-112">Updating the desktop image data</span></span>

<span data-ttu-id="e4fbe-113">DXGI 透過新的 [**IDXGIOutputDuplication：： AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) 方法，提供包含目前桌面映射的介面。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-113">DXGI provides a surface that contains a current desktop image through the new [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) method.</span></span> <span data-ttu-id="e4fbe-114">無論目前的顯示模式為何，桌面映射的格式一律為 [**DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-114">The format of the desktop image is always [**DXGI\_FORMAT\_B8G8R8A8\_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) no matter what the current display mode is.</span></span> <span data-ttu-id="e4fbe-115">除了這個介面，這些 [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) 方法會傳回指定的資訊類型，協助您判斷需要處理的介面中的哪些圖元：</span><span class="sxs-lookup"><span data-stu-id="e4fbe-115">Along with this surface, these [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) methods return the indicated types of info that help you determine which pixels within the surface you need to process:</span></span>

-   <span data-ttu-id="e4fbe-116">[**IDXGIOutputDuplication：： GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) 會傳回非重迭的區域，這是一種非重迭的矩形，指出作業系統自您處理先前的桌面映射後所更新的桌面映射區域。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-116">[**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) returns dirty regions, which are non-overlapping rectangles that indicate the areas of the desktop image that the operating system updated since you processed the previous desktop image.</span></span>
-   <span data-ttu-id="e4fbe-117">[**IDXGIOutputDuplication：： GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) 會傳回移動區域，也就是桌面映射中，作業系統移至相同映射內的另一個位置的矩形（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-117">[**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) returns move regions, which are rectangles of pixels in the desktop image that the operating system moved to another location within the same image.</span></span> <span data-ttu-id="e4fbe-118">每個移動區域都是由目的地矩形和來源點所組成。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-118">Each move region consists of a destination rectangle and a source point.</span></span> <span data-ttu-id="e4fbe-119">來源點會指定作業系統複製區域的位置，而目的地矩形會指定作業系統移至該區域的位置。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-119">The source point specifies the location from where the operating system copied the region and the destination rectangle specifies to where the operating system moved that region.</span></span> <span data-ttu-id="e4fbe-120">移動區域一律為非延伸區域，因此來源一律會與目的地相同。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-120">Move regions are always non-stretched regions so the source is always the same size as the destination.</span></span>

<span data-ttu-id="e4fbe-121">假設桌面映射是透過低速連線傳送至遠端用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-121">Suppose the desktop image was transmitted over a slow connection to your remote client app.</span></span> <span data-ttu-id="e4fbe-122">藉由只接收用戶端應用程式必須移動圖元區域（而非實際圖元資料）的資料，來減少透過連接傳送的資料量。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-122">The amount of data that is sent over the connection is reduced by receiving only data about how your client app must move regions of pixels rather than actual pixel data.</span></span> <span data-ttu-id="e4fbe-123">若要處理移動，您的用戶端應用程式必須已儲存完整的最後一個影像。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-123">To process the moves, your client app must have stored the complete last image.</span></span>

<span data-ttu-id="e4fbe-124">雖然作業系統會累積未處理的桌面映射更新，但它可能會用盡空間，以正確地儲存更新區域。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-124">While the operating system accumulates unprocessed desktop image updates, it might run out of space to accurately store the update regions.</span></span> <span data-ttu-id="e4fbe-125">在這種情況下，作業系統會將更新與現有的更新區域結合，以涵蓋所有新的更新，以開始累積更新。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-125">In this situation, the operating system starts to accumulate the updates by coalescing them with existing update regions to cover all new updates.</span></span> <span data-ttu-id="e4fbe-126">因此，作業系統所涵蓋的圖元尚未實際在該框架中更新。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-126">As a result, the operating system covers pixels that it has not actually updated in that frame yet.</span></span> <span data-ttu-id="e4fbe-127">但這種情況不會在您的用戶端應用程式上產生視覺問題，因為您會收到整個桌面映射，而不只是更新的圖元。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-127">But this situation doesn’t produce visual issues on your client app because you receive the entire desktop image and not just the updated pixels.</span></span>

<span data-ttu-id="e4fbe-128">若要重建正確的桌面映射，用戶端應用程式必須先處理所有的移動區域，然後處理所有中途區域。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-128">To reconstruct the correct desktop image, your client app must first process all the move regions and then process all the dirty regions.</span></span> <span data-ttu-id="e4fbe-129">這兩個中途和移動區域清單都可以完全空白。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-129">Either of these lists of dirty and move regions can be completely empty.</span></span> <span data-ttu-id="e4fbe-130">[桌面複製範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample)中的範例程式碼示範如何在單一框架中處理中途和移動區域：</span><span class="sxs-lookup"><span data-stu-id="e4fbe-130">The example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to process both the dirty and move regions in a single frame:</span></span>


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a><span data-ttu-id="e4fbe-131">旋轉桌面映射</span><span class="sxs-lookup"><span data-stu-id="e4fbe-131">Rotating the desktop image</span></span>

<span data-ttu-id="e4fbe-132">您必須將明確的程式碼新增至您的桌面複製用戶端應用程式，以支援旋轉模式。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-132">You must add explicit code to your desktop duplication client app to support rotated modes.</span></span> <span data-ttu-id="e4fbe-133">在旋轉模式中，從 [**IDXGIOutputDuplication：： AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) 收到的介面一律會處於未旋轉方向，而且桌面影像會在表面內旋轉。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-133">In a rotated mode, the surface that you receive from [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) is always in the un-rotated orientation, and the desktop image is rotated within the surface.</span></span> <span data-ttu-id="e4fbe-134">例如，如果桌面設定為以90度旋轉的768x1024， **AcquireNextFrame** 會傳回1024面，並在其中旋轉桌面影像。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-134">For example, if the desktop is set to 768x1024 at 90 degrees rotation, **AcquireNextFrame** returns a 1024x768 surface with the desktop image rotated within it.</span></span> <span data-ttu-id="e4fbe-135">以下是一些旋轉範例。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-135">Here are some rotation examples.</span></span>



| <span data-ttu-id="e4fbe-136">從顯示控制台設定的顯示模式</span><span class="sxs-lookup"><span data-stu-id="e4fbe-136">Display mode set from display control panel</span></span> | <span data-ttu-id="e4fbe-137">GDI 或 DXGI 傳回的顯示模式</span><span class="sxs-lookup"><span data-stu-id="e4fbe-137">Display mode returned by GDI or DXGI</span></span> | <span data-ttu-id="e4fbe-138">從 AcquireNextFrame 傳回的介面[ ](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span><span class="sxs-lookup"><span data-stu-id="e4fbe-138">Surface returned from [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)</span></span>                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fbe-139">1024x768 的橫向</span><span class="sxs-lookup"><span data-stu-id="e4fbe-139">1024x768 landscape</span></span>                          | <span data-ttu-id="e4fbe-140">1024 0 度旋轉</span><span class="sxs-lookup"><span data-stu-id="e4fbe-140">1024x768 0 degree rotation</span></span>           | <span data-ttu-id="e4fbe-141">1024 \[ 行\]</span><span class="sxs-lookup"><span data-stu-id="e4fbe-141">1024x768\[newline\]</span></span> ![nonrotated 遠端桌面](images/dxgi-outdupl-0-rotate.png)<br/>            |
| <span data-ttu-id="e4fbe-143">1024x768 縱向</span><span class="sxs-lookup"><span data-stu-id="e4fbe-143">1024x768 portrait</span></span>                           | <span data-ttu-id="e4fbe-144">768x1024 90 度數旋轉</span><span class="sxs-lookup"><span data-stu-id="e4fbe-144">768x1024 90 degree rotation</span></span>          | <span data-ttu-id="e4fbe-145">1024 \[ 行\]</span><span class="sxs-lookup"><span data-stu-id="e4fbe-145">1024x768\[newline\]</span></span> ![旋轉90度的遠端桌面](images/dxgi-outdupl-90-rotate.png)<br/>   |
| <span data-ttu-id="e4fbe-147"> (翻轉的1024x768 橫向) </span><span class="sxs-lookup"><span data-stu-id="e4fbe-147">1024x768 landscape (flipped)</span></span>                | <span data-ttu-id="e4fbe-148">1024x768 180 度旋轉</span><span class="sxs-lookup"><span data-stu-id="e4fbe-148">1024x768 180 degree rotation</span></span>         | <span data-ttu-id="e4fbe-149">1024 \[ 行\]</span><span class="sxs-lookup"><span data-stu-id="e4fbe-149">1024x768\[newline\]</span></span> ![旋轉180度的遠端桌面](images/dxgi-outdupl-180-rotate.png)<br/> |
| <span data-ttu-id="e4fbe-151"> (翻轉的1024x768 縱向) </span><span class="sxs-lookup"><span data-stu-id="e4fbe-151">1024x768 portrait (flipped)</span></span>                 | <span data-ttu-id="e4fbe-152">768x1024 270 度數旋轉</span><span class="sxs-lookup"><span data-stu-id="e4fbe-152">768x1024 270 degree rotation</span></span>         | <span data-ttu-id="e4fbe-153">1024 \[ 行\]</span><span class="sxs-lookup"><span data-stu-id="e4fbe-153">1024x768\[newline\]</span></span> ![旋轉270度的遠端桌面](images/dxgi-outdupl-270-rotate.png)<br/> |



 

<span data-ttu-id="e4fbe-155">您的桌面複製用戶端應用程式中的程式碼必須適當地旋轉桌面映射，才能顯示桌面映射。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-155">The code in your desktop duplication client app must rotate the desktop image appropriately before you display the desktop image.</span></span>

> [!Note]  
> <span data-ttu-id="e4fbe-156">在多重監視器案例中，您可以獨立輪替每個監視器的桌面映射。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-156">In multi-monitor scenarios, you can rotate the desktop image for each monitor independently.</span></span>

 

## <a name="updating-the-desktop-pointer"></a><span data-ttu-id="e4fbe-157">更新桌面指標</span><span class="sxs-lookup"><span data-stu-id="e4fbe-157">Updating the desktop pointer</span></span>

<span data-ttu-id="e4fbe-158">您需要使用桌面複製 API 來判斷用戶端應用程式是否必須將滑鼠指標圖形繪製到桌面影像。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-158">You need to use the desktop duplication API to determine if your client app must draw the mouse pointer shape onto the desktop image.</span></span> <span data-ttu-id="e4fbe-159">滑鼠指標已繪製至 [**IDXGIOutputDuplication：： AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) 提供的桌面影像，或滑鼠指標與桌面影像分開。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-159">Either the mouse pointer is already drawn onto the desktop image that [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) provides or the mouse pointer is separate from the desktop image.</span></span> <span data-ttu-id="e4fbe-160">如果滑鼠指標繪製在桌面影像上，則 *pFrameInfo* 參數所) 指向之 [**DXGI \_ OUTDUPL \_ 框架 \_ 資訊**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info)的 **PointerPosition** 成員中， **AcquireNextFrame** 所報告的指標位置資料 (會指出不會顯示個別指標。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-160">If the mouse pointer is drawn onto the desktop image, the pointer position data that is reported by **AcquireNextFrame** (in the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) that the *pFrameInfo* parameter points to) indicates that a separate pointer isn’t visible.</span></span> <span data-ttu-id="e4fbe-161">如果圖形介面卡在桌面影像上方重迭滑鼠指標， **AcquireNextFrame** 會報告顯示有個別指標。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-161">If the graphics adapter overlays the mouse pointer on top of the desktop image, **AcquireNextFrame** reports that a separate pointer is visible.</span></span> <span data-ttu-id="e4fbe-162">因此，您的用戶端應用程式必須將滑鼠指標圖形繪製到桌面影像上，以正確地表示目前使用者在其監視器上看到的內容。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-162">So, your client app must draw the mouse pointer shape onto the desktop image to accurately represent what the current user will see on their monitor.</span></span>

<span data-ttu-id="e4fbe-163">若要繪製桌面的滑鼠指標，請從 [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)的 *PFrameInfo* 參數使用 [**DXGI \_ OUTDUPL \_ 框架 \_ 資訊**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info)的 **PointerPosition** 成員，以決定要在桌面影像上的滑鼠指標左上角位置。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-163">To draw the desktop’s mouse pointer, use the **PointerPosition** member of [**DXGI\_OUTDUPL\_FRAME\_INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) from the *pFrameInfo* parameter of [**AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) to determine where to locate the top left hand corner of the mouse pointer on the desktop image.</span></span> <span data-ttu-id="e4fbe-164">當您繪製第一個框架時，您必須使用 [**IDXGIOutputDuplication：： GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) 方法來取得滑鼠指標圖形的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-164">When you draw the first frame, you must use the [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) method to obtain info about the shape of the mouse pointer.</span></span> <span data-ttu-id="e4fbe-165">每次呼叫 **AcquireNextFrame** 以取得下一個畫面格時，也會提供該框架目前的指標位置。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-165">Each call to **AcquireNextFrame** to get the next frame also provides the current pointer position for that frame.</span></span> <span data-ttu-id="e4fbe-166">另一方面，只有在圖形變更時，才需要再次使用 **GetFramePointerShape** 。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-166">On the other hand, you need to use **GetFramePointerShape** again only if the shape changes.</span></span> <span data-ttu-id="e4fbe-167">因此，請保留最後一個指標影像的複本，並使用它在桌面上繪製，除非滑鼠指標的形狀有所變更。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-167">So, keep a copy of the last pointer image and use it to draw on the desktop unless the shape of the mouse pointer changes.</span></span>

> [!Note]  
> <span data-ttu-id="e4fbe-168">[**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)會搭配指標圖形影像，提供作用點位置的大小。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-168">Together with the pointer shape image, [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) provides the size of the hot spot location.</span></span> <span data-ttu-id="e4fbe-169">此作用點僅供資訊參考之用。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-169">The hot spot is given for informational purposes only.</span></span> <span data-ttu-id="e4fbe-170">要在其中繪製指標影像的位置與熱點無關。</span><span class="sxs-lookup"><span data-stu-id="e4fbe-170">The location of where to draw the pointer image is independent to the hotspot.</span></span>

 

<span data-ttu-id="e4fbe-171">這段來自 [桌面複製範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) 的程式碼範例示範如何取得滑鼠指標圖形：</span><span class="sxs-lookup"><span data-stu-id="e4fbe-171">This example code from the [Desktop Duplication Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) shows how to get the mouse pointer shape:</span></span>


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e4fbe-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="e4fbe-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4fbe-173">DXGI 1.2 改進</span><span class="sxs-lookup"><span data-stu-id="e4fbe-173">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
