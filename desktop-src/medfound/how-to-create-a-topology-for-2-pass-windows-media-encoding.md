---
description: 特定 Windows 媒體編碼器和管線層媒體基礎支援兩種編碼模式。
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: 如何建立 Two-Pass Windows Media 編碼的拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945631"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a><span data-ttu-id="ca6b8-103">如何建立 Two-Pass Windows Media 編碼的拓撲</span><span class="sxs-lookup"><span data-stu-id="ca6b8-103">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>

<span data-ttu-id="ca6b8-104">特定 Windows 媒體編碼器和管線層媒體基礎支援兩種編碼模式。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-104">Two-pass encoding modes are supported by certain Windows Media encoders and Media Foundation at the pipeline layer.</span></span> <span data-ttu-id="ca6b8-105">應用程式必須設定和設定類似于單一傳遞編碼方式的編碼拓撲，但在雙通路編碼模式中，應用程式必須執行編碼會話兩次。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-105">The application must configure and set up the encoding topology similar to that in single-pass encoding but in the 2-pass encoding mode, the application must run the encoding session twice.</span></span> <span data-ttu-id="ca6b8-106">在第一次通過時，編碼器會收集有關串流內容的資訊。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-106">On the first pass, the encoder gathers information about the content of the stream.</span></span> <span data-ttu-id="ca6b8-107">在第二個階段，藉由使用第一次傳遞時所收集的資訊，會產生最終的輸出檔。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-107">On the second pass, by using the information gathered on the first pass, the final output file is generated.</span></span> <span data-ttu-id="ca6b8-108">藉由處理資料流程的範例兩次，兩次傳遞編碼會將編碼程式優化，並產生更高品質的編碼檔案。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-108">By processing the samples for the stream twice, two-pass encoding optimizes the encoding process and produces higher quality encoded files.</span></span> <span data-ttu-id="ca6b8-109">無法在即時資料流上使用雙向編碼模式。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-109">Two-pass encoding modes cannot be used on live streams.</span></span>

<span data-ttu-id="ca6b8-110">媒體基礎支援下列兩個傳遞的編碼模式：</span><span class="sxs-lookup"><span data-stu-id="ca6b8-110">Media Foundation supports the following two-pass encoding modes:</span></span>

-   [<span data-ttu-id="ca6b8-111">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="ca6b8-111">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="ca6b8-112">尖峰限制的可變位速率編碼</span><span class="sxs-lookup"><span data-stu-id="ca6b8-112">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md)

<span data-ttu-id="ca6b8-113">建立雙通路編碼的編碼拓撲類似于單一傳遞模式。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-113">Building an encoding topology for two-pass encoding is similar to single pass modes.</span></span> <span data-ttu-id="ca6b8-114">下列清單顯示主要的差異。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-114">The following list shows the key differences.</span></span>

-   <span data-ttu-id="ca6b8-115">編碼器設定必須包含設定為2的 [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md) 屬性，以及 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 屬性設為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-115">Encoder configuration must include the [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md) property that is set to 2 and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="ca6b8-116">這會將編碼器的功能篩選為雙通路模式。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-116">This filters the encoder’s capabilities to two-pass modes.</span></span> <span data-ttu-id="ca6b8-117">如果您使用的是啟用物件，請將這些屬性傳遞至 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-117">If you are using activation objects, pass these properties to [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>
-   <span data-ttu-id="ca6b8-118">針對第一次傳遞，請在輸出節點中使用虛擬媒體接收，因為在此階段中產生的範例不會加入至最終檔案。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-118">For the first pass, use a dummy media sink in the output node because the samples that are generated in this pass are not added to the final file.</span></span>
-   <span data-ttu-id="ca6b8-119">針對第二個階段，查詢編碼器中是否有必要的編碼後內容，並以設定這些屬性的 ASF 媒體接收器取代 [虛擬媒體接收] 節點。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-119">For the second pass, query the encoder for the required post-encoding properties and replace the dummy media sink node with the ASF media sink with these properties set.</span></span>

<span data-ttu-id="ca6b8-120">如需設定編碼拓撲的詳細資訊，請參閱 [教學課程：單一傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-120">For more information about setting up an encoding topology see, [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).</span></span>

<span data-ttu-id="ca6b8-121">下列程式摘要說明在 ASF 容器中使用雙向編碼模式來編碼 Windows Media 內容的步驟。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-121">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a two-pass encoding mode.</span></span>

1.  <span data-ttu-id="ca6b8-122">使用來源解析程式建立所指定的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-122">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="ca6b8-123">列舉媒體來源中的串流。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-123">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="ca6b8-124">根據媒體來源中需要編碼的資料流程，建立 ASF 媒體接收器並新增資料流程接收器。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-124">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="ca6b8-125">建立媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-125">Create the media sink.</span></span>
5.  <span data-ttu-id="ca6b8-126">在輸出檔中建立資料流程的 Windows Media 編碼器。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-126">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="ca6b8-127">使用2傳遞編碼屬性來設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-127">Configure the encoders with the 2-pass encoding properties.</span></span>
7.  <span data-ttu-id="ca6b8-128">藉由連接來源、編碼器和媒體接收器來建立部分編碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-128">Build a partial encoding topology by connecting the source, encoders, and the media sink.</span></span>
8.  <span data-ttu-id="ca6b8-129">將媒體會話具現化，並在媒體會話上設定拓撲。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-129">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="ca6b8-130">藉由控制媒體會話並從媒體會話取得所有相關事件，來執行第一個編碼階段。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-130">Run the first encoding pass by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="ca6b8-131">關閉並關閉編碼會話。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-131">Close and shutdown the encoding session.</span></span>
11. <span data-ttu-id="ca6b8-132">根據編碼類型，查詢編碼器中的下列屬性：</span><span class="sxs-lookup"><span data-stu-id="ca6b8-132">Query the encoder for the following properties depending on the type of encoding:</span></span> 

    | <span data-ttu-id="ca6b8-133">編碼類型</span><span class="sxs-lookup"><span data-stu-id="ca6b8-133">Encoding type</span></span>                                                                                        | <span data-ttu-id="ca6b8-134">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ca6b8-134">Property name</span></span>                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="ca6b8-135">不受限制的變數位速率編碼</span><span class="sxs-lookup"><span data-stu-id="ca6b8-135">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | [<span data-ttu-id="ca6b8-136">**MFPKEY \_ PASSESUSED**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-136">**MFPKEY\_PASSESUSED**</span></span>](mfpkey-passesusedproperty.md)<br/> [<span data-ttu-id="ca6b8-137">**MFPKEY \_ VBRENABLED**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-137">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)<br/> [<span data-ttu-id="ca6b8-138">**MFPKEY \_ BAVG**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-138">**MFPKEY\_BAVG**</span></span>](mfpkey-bavgproperty.md)<br/> [<span data-ttu-id="ca6b8-139">**MFPKEY \_ RAVG**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-139">**MFPKEY\_RAVG**</span></span>](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [<span data-ttu-id="ca6b8-140">尖峰限制的可變位速率編碼</span><span class="sxs-lookup"><span data-stu-id="ca6b8-140">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | [<span data-ttu-id="ca6b8-141">**MFPKEY \_ PASSESUSED**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-141">**MFPKEY\_PASSESUSED**</span></span>](mfpkey-passesusedproperty.md)<br/> [<span data-ttu-id="ca6b8-142">**MFPKEY \_ VBRENABLED**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-142">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)<br/> [<span data-ttu-id="ca6b8-143">**MFPKEY \_ BAVG**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-143">**MFPKEY\_BAVG**</span></span>](mfpkey-bavgproperty.md)<br/> [<span data-ttu-id="ca6b8-144">**MFPKEY \_ RAVG**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-144">**MFPKEY\_RAVG**</span></span>](mfpkey-ravgproperty.md)<br/> [<span data-ttu-id="ca6b8-145">**MFPKEY \_ BMAX**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-145">**MFPKEY\_BMAX**</span></span>](mfpkey-bmaxproperty.md)<br/> [<span data-ttu-id="ca6b8-146">**MFPKEY \_ RMAX**</span><span class="sxs-lookup"><span data-stu-id="ca6b8-146">**MFPKEY\_RMAX**</span></span>](mfpkey-rmaxproperty.md)<br/> |

    

     

12. <span data-ttu-id="ca6b8-147">根據您想要包含在最終輸出檔中的資料流程，建立 ASF 檔案接收並新增必要的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-147">Create the ASF file sink and add the required stream sinks depending on the streams you want to include in the final output file.</span></span>
13. <span data-ttu-id="ca6b8-148">在步驟11中，設定在檔接收器上抓取的編碼器屬性。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-148">Set the encoder properties retrieved in step 11 on the file sink.</span></span>
14. <span data-ttu-id="ca6b8-149">將輸出節點中的媒體接收器取代為新建立的檔案接收。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-149">Replace the media sink in the output node with the newly created file sink.</span></span>
15. <span data-ttu-id="ca6b8-150">將媒體會話具現化，並在媒體會話上設定更新的拓撲。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-150">Instantiate the Media Session and set the updated topology on the Media Session.</span></span>
16. <span data-ttu-id="ca6b8-151">藉由控制媒體會話並從媒體會話取得所有相關事件，來執行第二次編碼階段。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-151">Run second encoding pass by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
17. <span data-ttu-id="ca6b8-152">等候來自媒體會話的 [MEEndOfPresentation](meendofpresentation.md) 事件，然後在事件處理常式中取得編碼器的編碼屬性值，並在檔案接收上進行設定。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-152">Wait for the [MEEndOfPresentation](meendofpresentation.md) event from the Media Session and in the event handler get the encoding property values from the encoder and set them on the file sink.</span></span> <span data-ttu-id="ca6b8-153">如需詳細資訊，請參閱 [教學課程：單一傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)中的「更新 File 接收器中的編碼屬性」。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-153">For more information, see "Update Encoding Properties in the File Sink" in [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).</span></span>
18. <span data-ttu-id="ca6b8-154">關閉並關閉編碼會話。</span><span class="sxs-lookup"><span data-stu-id="ca6b8-154">Close and shutdown the encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca6b8-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca6b8-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca6b8-156">管線層 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="ca6b8-156">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




