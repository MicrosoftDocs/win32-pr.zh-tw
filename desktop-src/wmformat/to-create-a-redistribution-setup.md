---
title: 若要建立轉散發設定
description: 若要建立轉散發設定
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK，軟體轉散發
- Advanced Systems Format (ASF) 、軟體轉散發
- ASF (Advanced Systems Format) ，軟體轉散發
- Windows Media Format SDK，轉散發
- Advanced Systems Format (ASF) ，轉散發
- ASF (Advanced Systems Format) ，轉散發
- 軟體轉散發，建立
- 軟體轉散發，WMFDist.exe
- 轉散發，建立
- 轉散發，WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183435"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="32965-114">若要建立轉散發設定</span><span class="sxs-lookup"><span data-stu-id="32965-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="32965-115">讓您的安裝程式常式先安裝應用程式檔，並進行必要的設定，再叫用轉散發套件。</span><span class="sxs-lookup"><span data-stu-id="32965-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="32965-116">安裝 WMFDist.exe。</span><span class="sxs-lookup"><span data-stu-id="32965-116">Install WMFDist.exe.</span></span> <span data-ttu-id="32965-117">您可以使用/Q：旗標來執行無訊息自動安裝，並在應用程式安裝期間隱藏轉散發安裝程式的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="32965-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="32965-118">然後，您的常式必須偵測到結束時是否需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="32965-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="32965-119">例如：</span><span class="sxs-lookup"><span data-stu-id="32965-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="32965-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="32965-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32965-121">**軟體轉散發**</span><span class="sxs-lookup"><span data-stu-id="32965-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




