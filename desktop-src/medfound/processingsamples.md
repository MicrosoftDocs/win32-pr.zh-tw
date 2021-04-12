---
description: 處理編解碼器 SQL-DMO 輸入和輸出
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: 處理編解碼器 SQL-DMO 輸入和輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318740"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="4c503-103">處理編解碼器 SQL-DMO 輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="4c503-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="4c503-104">當您已設定了一類的輸入類型和輸出類型時，就可以開始處理資料範例。</span><span class="sxs-lookup"><span data-stu-id="4c503-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="4c503-105">您可以使用 **IMediaObject：:P rocessinput** 方法，將範例傳遞給 sql-dmo 以進行處理，然後藉由呼叫 **IMediaObject：:P rocessoutput** 來取得已處理的範例。</span><span class="sxs-lookup"><span data-stu-id="4c503-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="4c503-106">您應該為所有傳遞的輸入樣本設定正確的時間戳記和持續時間。</span><span class="sxs-lookup"><span data-stu-id="4c503-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="4c503-107">時間戳記並非絕對必要，但有助於維護音訊/影片同步處理。</span><span class="sxs-lookup"><span data-stu-id="4c503-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="4c503-108">如果您沒有範例的時間戳記，最好不要將其保留，而不是使用不確定的值。</span><span class="sxs-lookup"><span data-stu-id="4c503-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c503-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c503-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c503-110">使用編解碼器 DMOs</span><span class="sxs-lookup"><span data-stu-id="4c503-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



