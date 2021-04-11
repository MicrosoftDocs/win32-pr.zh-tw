---
description: 處理編解碼器 MFT 輸入和輸出
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: 處理編解碼器 MFT 輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191761"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="73267-103">處理編解碼器 MFT 輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="73267-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="73267-104">當您設定了 MFT 的輸入類型和輸出類型時，就可以開始處理資料範例。</span><span class="sxs-lookup"><span data-stu-id="73267-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="73267-105">您可以使用 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 方法，將範例傳遞給 MFT 以進行處理，然後藉由呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)來取得已處理的範例。</span><span class="sxs-lookup"><span data-stu-id="73267-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="73267-106">您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。</span><span class="sxs-lookup"><span data-stu-id="73267-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="73267-107">時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。</span><span class="sxs-lookup"><span data-stu-id="73267-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="73267-108">如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。</span><span class="sxs-lookup"><span data-stu-id="73267-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73267-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="73267-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73267-110">使用編解碼器 MFTs</span><span class="sxs-lookup"><span data-stu-id="73267-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



