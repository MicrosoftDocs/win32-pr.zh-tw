---
description: 從檔案傳輸 DV 到磁帶
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: 從檔案傳輸 DV 到磁帶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984654"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="bad1d-103">從檔案傳輸 DV 到磁帶</span><span class="sxs-lookup"><span data-stu-id="bad1d-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="bad1d-104">從 DV AVI 檔傳輸到 VTR 磁帶有點複雜，因為檔案可以輸入-1 或類型2。</span><span class="sxs-lookup"><span data-stu-id="bad1d-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="bad1d-105">若要將 DV 檔案傳送至磁帶，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="bad1d-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="bad1d-106">建立 [MSDV 驅動程式](msdv-driver.md) 篩選器的實例。</span><span class="sxs-lookup"><span data-stu-id="bad1d-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="bad1d-107">如需詳細資訊，請參閱 [選取擷取裝置](selecting-a-capture-device.md)。</span><span class="sxs-lookup"><span data-stu-id="bad1d-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="bad1d-108">請確定裝置處於 VTR 模式。</span><span class="sxs-lookup"><span data-stu-id="bad1d-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="bad1d-109">否則，您無法傳輸至磁帶。請參閱 [裝置模式](device-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="bad1d-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="bad1d-110">如 [關於 Capture graph](about-the-capture-graph-builder.md)產生器中所述，初始化 Capture graph builder。</span><span class="sxs-lookup"><span data-stu-id="bad1d-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="bad1d-111">建立圖形。</span><span class="sxs-lookup"><span data-stu-id="bad1d-111">Build the graph.</span></span> <span data-ttu-id="bad1d-112">圖形設定取決於 DV 檔案類型：</span><span class="sxs-lookup"><span data-stu-id="bad1d-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="bad1d-113">從類型1檔案傳輸</span><span class="sxs-lookup"><span data-stu-id="bad1d-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="bad1d-114">從類型2檔案傳輸</span><span class="sxs-lookup"><span data-stu-id="bad1d-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="bad1d-115">將裝置進入記錄暫停模式，如 [控制 DV](controlling-a-dv-camcorder.md)攝影機所述。</span><span class="sxs-lookup"><span data-stu-id="bad1d-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="bad1d-116">暫停篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="bad1d-116">Pause the filter graph.</span></span> <span data-ttu-id="bad1d-117">當篩選圖形暫停時，它會傳送連續的資料流程，以重複第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="bad1d-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="bad1d-118">若要開始傳輸，請將裝置放入記錄模式，然後執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="bad1d-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="bad1d-119">它會將裝置設為一定的時間，直到記錄標頭能夠錄製為止，因此請等候大約兩秒，然後再執行圖形。</span><span class="sxs-lookup"><span data-stu-id="bad1d-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="bad1d-120">這可能會導致磁帶的開頭有幾個重複的畫面格，但它可確保不會遺失任何資料。</span><span class="sxs-lookup"><span data-stu-id="bad1d-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bad1d-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="bad1d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad1d-122">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="bad1d-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



