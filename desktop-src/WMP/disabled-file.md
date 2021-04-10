---
title: 停用的檔案
description: 停用的檔案
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Windows Media Player 行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 面板的美工檔案，已停用的檔案
- Windows Media Player 行動外觀、已停用的檔案
- 外觀，已停用的檔案
- 面板中已停用的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021698"
---
# <a name="disabled-file"></a><span data-ttu-id="62f0d-110">停用的檔案</span><span class="sxs-lookup"><span data-stu-id="62f0d-110">Disabled File</span></span>

<span data-ttu-id="62f0d-111">停用的檔案包含當無法使用特定按鈕函式或關閉按鈕狀態時將顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="62f0d-111">The Disabled file contains the images that will be displayed when a particular button function cannot be used or a button state is off.</span></span> <span data-ttu-id="62f0d-112">例如，如果定義了空白的播放清單，則會顯示 [ **下一步]** 和 [ **上** 一個] 按鈕，而且應該使用停用的影像來顯示。</span><span class="sxs-lookup"><span data-stu-id="62f0d-112">For example, if an empty playlist is defined, the **Next** and **Prev** buttons will be displayed, and they should be displayed using a disabled image.</span></span> <span data-ttu-id="62f0d-113">此外，針對切換按鈕，已停用的影像會用來指出狀態為 [關閉]。</span><span class="sxs-lookup"><span data-stu-id="62f0d-113">Also, for toggle buttons, the Disabled image is used to indicate that the state is off.</span></span>

<span data-ttu-id="62f0d-114">下圖是一般停用的檔案。</span><span class="sxs-lookup"><span data-stu-id="62f0d-114">The following image is a typical Disabled file.</span></span>

![停用的檔案](images/cesdkdis.png)

<span data-ttu-id="62f0d-116">這會儲存已停用的點擊類型按鈕影像。</span><span class="sxs-lookup"><span data-stu-id="62f0d-116">This stores the images for hit-type buttons that are disabled.</span></span> <span data-ttu-id="62f0d-117">影像類似于背景檔案，但色彩較淺。</span><span class="sxs-lookup"><span data-stu-id="62f0d-117">The images are similar to the Background file, but the colors are lighter.</span></span> <span data-ttu-id="62f0d-118">使用在外觀定義檔案的點陣圖區段中定義的位移，按鈕影像會與背景檔案影像對齊。</span><span class="sxs-lookup"><span data-stu-id="62f0d-118">Using the offset defined in the Bitmaps section of the skin definition file, the button images line up with the Background file image.</span></span>

<span data-ttu-id="62f0d-119">請注意，按鈕影像的背景完全符合背景檔案中對應的區域。</span><span class="sxs-lookup"><span data-stu-id="62f0d-119">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="62f0d-120">這點很重要，因為當 [點擊類型] 按鈕無法使用時，為停用的影像定義的整個矩形將會取代背景檔案中的相符區域。</span><span class="sxs-lookup"><span data-stu-id="62f0d-120">This is important, because when a hit-type button is unavailable, the entire rectangle defined for the disabled image will replace the matching area in the Background file.</span></span> <span data-ttu-id="62f0d-121">讓圖形保持與背景影像一致，以確保只有您想要顯示的按鈕部分會實際變更。</span><span class="sxs-lookup"><span data-stu-id="62f0d-121">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62f0d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="62f0d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62f0d-123">**美工檔案**</span><span class="sxs-lookup"><span data-stu-id="62f0d-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




