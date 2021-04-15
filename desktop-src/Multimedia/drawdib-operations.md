---
title: DrawDib 作業
description: DrawDib 作業
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib，關於
- DrawDib，存取
- DrawDib，開啟
- DrawDib，作業
- 'DrawDib，裝置內容 (DC) '
- 'DC (裝置內容) '
- DrawDibOpen 函式
- DrawDibClose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462461"
---
# <a name="drawdib-operations"></a><span data-ttu-id="62594-111">DrawDib 作業</span><span class="sxs-lookup"><span data-stu-id="62594-111">DrawDib Operations</span></span>

<span data-ttu-id="62594-112">您可以使用 [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) 函數來存取整個 DrawDib 函數群組。</span><span class="sxs-lookup"><span data-stu-id="62594-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="62594-113">此函式會載入動態連結程式庫 (DLL) 、配置記憶體資源、建立 DrawDib 的裝置內容 (DC) ，以及維護已初始化之 Dc 數目的參考計數。</span><span class="sxs-lookup"><span data-stu-id="62594-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="62594-114">**DrawDibOpen** 也會傳回您搭配其他 DrawDib 函式使用之新 DC 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="62594-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="62594-115">當您完成使用 [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) 函式時，可以釋放 DrawDib DC。</span><span class="sxs-lookup"><span data-stu-id="62594-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="62594-116">**DrawDibClose** 也會減少存取 DLL 之應用程式的參考計數。</span><span class="sxs-lookup"><span data-stu-id="62594-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="62594-117">對 **DrawDibClose** 的呼叫應該是您應用程式中的最後一個 DrawDib 函數。</span><span class="sxs-lookup"><span data-stu-id="62594-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="62594-118">您可以依需要建立任意數量的 DrawDib Dc。</span><span class="sxs-lookup"><span data-stu-id="62594-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="62594-119">您可以使用多個 DrawDib Dc 來同時繪製數個位圖。</span><span class="sxs-lookup"><span data-stu-id="62594-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="62594-120">您也可以建立多個 DrawDib Dc，各有獨特的特性，讓您的應用程式可以選擇，然後使用具有最適當設定的 DC。</span><span class="sxs-lookup"><span data-stu-id="62594-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="62594-121">例如，您可以在應用程式中建立兩個 DrawDib Dc：一個是以正常解析度顯示影像，另一個則顯示影像的放大部分。</span><span class="sxs-lookup"><span data-stu-id="62594-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="62594-122">若要有效率地執行，DrawDib 函式需要顯示介面卡及其驅動程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="62594-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="62594-123">在第一次存取包含 DrawDib 函式的 DLL 時，會在顯示介面卡上執行一系列測試來取得顯示設定檔。</span><span class="sxs-lookup"><span data-stu-id="62594-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="62594-124">DrawDib 函式會將此資訊用於所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="62594-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="62594-125">您可以使用 [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) 函式，視需要重複這些測試。</span><span class="sxs-lookup"><span data-stu-id="62594-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="62594-126">抓取和儲存顯示設定檔通常是一次出現。</span><span class="sxs-lookup"><span data-stu-id="62594-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="62594-127">但是，如果已刪除設定檔資訊或系統中安裝了另一個顯示驅動程式，DrawDib 會重新運行測試。</span><span class="sxs-lookup"><span data-stu-id="62594-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="62594-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="62594-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62594-129">關於 DrawDib 函式</span><span class="sxs-lookup"><span data-stu-id="62594-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




