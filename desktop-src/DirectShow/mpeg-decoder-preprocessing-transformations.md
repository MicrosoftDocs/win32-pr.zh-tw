---
description: MPEG 解碼器前置處理轉換
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: MPEG 解碼器前置處理轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908896"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="8d90f-103">MPEG 解碼器前置處理轉換</span><span class="sxs-lookup"><span data-stu-id="8d90f-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="8d90f-104">**黑邊和 PanScan**</span><span class="sxs-lookup"><span data-stu-id="8d90f-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="8d90f-105">4x3 影像的組成方式，是將影像的頂端和底部填補 (稱為黑邊影像) 或藉由將影像的4x3 部分解壓縮 (稱為 PanScan 影像) 。</span><span class="sxs-lookup"><span data-stu-id="8d90f-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="8d90f-106">功能表和子圖片串流會在最後的影片影像上方重迭。</span><span class="sxs-lookup"><span data-stu-id="8d90f-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="8d90f-107">16x9 比例影像會以 4x3 anamorphic 格式儲存。</span><span class="sxs-lookup"><span data-stu-id="8d90f-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="8d90f-108">將 anamorphic 4x3 外觀比例720x480 來源影片延伸至16x9 的外觀比例，形成原始的16x9 外觀影像。</span><span class="sxs-lookup"><span data-stu-id="8d90f-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="8d90f-109">以下說明如何正確地顯示每個模式及其重點：</span><span class="sxs-lookup"><span data-stu-id="8d90f-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="8d90f-110">**寬銀幕：** 來源影片會延伸至 [輸出] 視窗的最大16x9 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="8d90f-111">重點是相對於16x9 區域內的。</span><span class="sxs-lookup"><span data-stu-id="8d90f-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="8d90f-112">黑色橫條應該加入至頂端和底部或側邊，以維護16x9 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="8d90f-113">**平移掃描：** 從16x9 影片中，使用 MPEG2 串流中提供的水準位移，將4x3 子視窗解壓縮。</span><span class="sxs-lookup"><span data-stu-id="8d90f-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="8d90f-114">將4x3 子視窗放到輸出用戶端視窗的最大4x3 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="8d90f-115">醒目提示的座標是相對於4x3 輸出視窗，與來源16x9 影片沒有任何關聯性。</span><span class="sxs-lookup"><span data-stu-id="8d90f-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="8d90f-116">黑色橫條應該加入至頂端和底部或側邊，以維護4x3 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="8d90f-117">**黑邊：** 計算輸出視窗的最大4x3 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="8d90f-118">黑色橫條應該加入至頂端和底部或側邊，以維護4x3 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="8d90f-119">來源 anamorphic 4x3 影片 (代表16x9 影像) 放置在4x3 區域內的最大16x9 子視窗中。</span><span class="sxs-lookup"><span data-stu-id="8d90f-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="8d90f-120">黑色橫條應新增至子視窗的頂端和底部，以維護16x9 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="8d90f-121">醒目提示的座標是相對於4x3 區域，沒有與來源16x9 影片的關聯性。</span><span class="sxs-lookup"><span data-stu-id="8d90f-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="8d90f-122">磁片可能會在16x9 區域以外的地方指定醒目提示 (但仍在 [4x3] 視窗) 。</span><span class="sxs-lookup"><span data-stu-id="8d90f-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="8d90f-123">針對 4x3 video，影片會放在輸出用戶端視窗的最大4x3 輸出區域中。</span><span class="sxs-lookup"><span data-stu-id="8d90f-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="8d90f-124">黑色橫條應該加入至頂端和底部或側邊，以維護4x3 區域。</span><span class="sxs-lookup"><span data-stu-id="8d90f-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="8d90f-125">**使用 DVD 導覽器和 VMR 的 MPEG 前置處理**</span><span class="sxs-lookup"><span data-stu-id="8d90f-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="8d90f-126">目前，解碼器會傳遞格式 \_ MPEG2 \_ 影片媒體類型 (其格式區塊指向 [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) 結構) 。</span><span class="sxs-lookup"><span data-stu-id="8d90f-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="8d90f-127">在輸出針腳上，此解碼器會產生格式 \_ VideoInfo2 的媒體類型，其格式區塊會指向 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構。</span><span class="sxs-lookup"><span data-stu-id="8d90f-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="8d90f-128">結構的 **>dwreserved** 欄位已重新命名為 **dwControls** 旗標。</span><span class="sxs-lookup"><span data-stu-id="8d90f-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="8d90f-129">**DwControlFlags** 成員現在會包含新的位。</span><span class="sxs-lookup"><span data-stu-id="8d90f-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="8d90f-130">標籤</span><span class="sxs-lookup"><span data-stu-id="8d90f-130">Label</span></span> | <span data-ttu-id="8d90f-131">值</span><span class="sxs-lookup"><span data-stu-id="8d90f-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="8d90f-132">使用的 AMCONTROL \_</span><span class="sxs-lookup"><span data-stu-id="8d90f-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="8d90f-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8d90f-133">0x00000001</span></span> |
| <span data-ttu-id="8d90f-134">AMCONTROL \_ PAD \_ 至 \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="8d90f-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="8d90f-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8d90f-135">0x00000002</span></span> |
| <span data-ttu-id="8d90f-136">AMCONTROL \_ PAD \_ 至 \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="8d90f-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="8d90f-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8d90f-137">0x00000004</span></span> |



 

<span data-ttu-id="8d90f-138">\_使用的 AMCONTROL 可用來測試是否支援這些新的旗標。</span><span class="sxs-lookup"><span data-stu-id="8d90f-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="8d90f-139">來源篩選器應設定 AMCONTROL \_ 使用旗標，並查看 QueryAccept (媒體) 是否在下游 pin 上成功。</span><span class="sxs-lookup"><span data-stu-id="8d90f-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="8d90f-140">如果拒絕，則無法使用 AMCONTROL 旗標，而且 dwReserved1 必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="8d90f-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="8d90f-141">AMCONTROL \_ PAD \_ TO \_ 4x3 指出影像應該填補並顯示在4x3 區域中。</span><span class="sxs-lookup"><span data-stu-id="8d90f-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="8d90f-142">AMCONTROL \_ PAD \_ TO \_ 16x9 指出影像應該填補並顯示在16x9 區域中。</span><span class="sxs-lookup"><span data-stu-id="8d90f-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="8d90f-143">此解碼器應該盲目地複製或處理位。</span><span class="sxs-lookup"><span data-stu-id="8d90f-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="8d90f-144">如果此解碼器本身執行上下黑邊縮，則必須改變圖元外觀比例、填補影像，並移除對應的 AMCONTROL \_ \* 位。</span><span class="sxs-lookup"><span data-stu-id="8d90f-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="8d90f-145">MPEG2VIDEOINFO. dwFlags 現在包含三個旗標，可用來控制內容的顯示方式：</span><span class="sxs-lookup"><span data-stu-id="8d90f-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="8d90f-146">`AMMPEG2_DoPanScan (0x00000001)`：如果已設定此旗標，則 MPEG-2 視頻解碼器應該根據圖片顯示延伸模組中的平移掃描向量來裁剪輸出 \_ 影像 \_ ，並將圖片外觀比例變更為4x3。</span><span class="sxs-lookup"><span data-stu-id="8d90f-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="8d90f-147">VMR 不應該收到具有此旗標的16x9 範例。</span><span class="sxs-lookup"><span data-stu-id="8d90f-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="8d90f-148">簡單的實作為可能會改變來源矩形，以指出具有左邊緣等於圖片顯示延伸模組中顯示位移的540寬來源 \_ 區域 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8d90f-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="8d90f-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`：當硬體解碼器將此資料流程顯示為影片輸出時 (通常是卡片) 上的 SVIDEO 連接器，它應該套用規則，以顯示4x3 顯示器上的16x9 範例。</span><span class="sxs-lookup"><span data-stu-id="8d90f-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="8d90f-150">軟體解碼器 (或產生傳送至 VMR) 之輸出的硬體解碼器，在處理影像時有兩個選項：</span><span class="sxs-lookup"><span data-stu-id="8d90f-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="8d90f-151">忽略此旗標，並將 VideoInfoHeader2 內容傳遞至 VMR (AMCONTROL \_ PAD \_ to \_ 4x3 旗標將已由) 範例的 [DVD 導覽器](dvd-navigator-filter.md) 設定。</span><span class="sxs-lookup"><span data-stu-id="8d90f-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="8d90f-152">VMR 將會遇到 16x9 video 範例，其中包含 AMCONTROL \_ PAD \_ TO \_ 4x3 旗標以及4x3 子圖片 stream。</span><span class="sxs-lookup"><span data-stu-id="8d90f-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="8d90f-153">應用程式必須將兩個數據流的輸出正規化目的矩形設定為相同的寬度。</span><span class="sxs-lookup"><span data-stu-id="8d90f-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="8d90f-154">藉由填補影像的頂端和底部，並將影像外觀比例設定為 4x3 (請參閱) 上述黑邊，並將 AMCONTROL 板從4x3 移除 VIDEOINFOHEADER2 位，以將 anamorphic 資料流程轉換成4x3 影像 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8d90f-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="8d90f-155">Blend 影片和子圖片資料流程的 DirectXVA 解碼器將必須處理此旗標。</span><span class="sxs-lookup"><span data-stu-id="8d90f-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="8d90f-156">如果硬體無法調整混合的子圖片，則該解碼器應該產生個別的子圖片資料流程，讓 VMR 與影片 blend。</span><span class="sxs-lookup"><span data-stu-id="8d90f-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="8d90f-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`：當硬體解碼器將此資料流程顯示為視頻輸出時 (通常是卡片) 上的 SVIDEO 連接器，它應該假設 16x9 (anamorphic) 顯示。</span><span class="sxs-lookup"><span data-stu-id="8d90f-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="8d90f-158">軟體解碼器 (，或產生傳送至 VMR) 之輸出的硬體解碼器，在處理 anamorphic 映射時有兩個選項：</span><span class="sxs-lookup"><span data-stu-id="8d90f-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="8d90f-159">忽略此旗標，並將 VideoInfoHeader2 內容複寫到 VMR。</span><span class="sxs-lookup"><span data-stu-id="8d90f-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="8d90f-160">VMR 會將4x3 影像填補至16x9 （如果有 AMCONTROL \_ pad） \_ \_ 16x9 設定。</span><span class="sxs-lookup"><span data-stu-id="8d90f-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="8d90f-161">將輸出影像填補至16x9 影像，並將 AMCONTROL \_ PAD 移 \_ 至 \_ 16x9 位。</span><span class="sxs-lookup"><span data-stu-id="8d90f-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="8d90f-162">大部分的解碼器都應該使用 **GetMediaType** 來偵測輸入釘選上的媒體變更，並將 **MPEG2INFOHEADER**) 包含的 **VIDEOINFOHEADER2** (內容複寫到輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8d90f-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="8d90f-163">它們可能只會處理 PanScan 位。</span><span class="sxs-lookup"><span data-stu-id="8d90f-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="8d90f-164">下列範例程式碼示範如何將 **VIDEOINFOHEADER2** 內容從輸入釘選到輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="8d90f-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



