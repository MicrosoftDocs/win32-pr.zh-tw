---
title: 取得壓縮機和 Decompressors 的相關資訊
description: 取得壓縮機和 Decompressors 的相關資訊
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，取得有關壓縮機的資訊
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，取得有關壓縮機的資訊
- ICGetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932259"
---
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="70773-106">取得壓縮機和 Decompressors 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="70773-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="70773-107">若要取得有關壓縮程式或解壓縮程式的一般資訊，您的應用程式可以使用 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="70773-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="70773-108">此函式會填入 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) 結構，其中包含有關壓縮程式或解壓縮程式的資訊。</span><span class="sxs-lookup"><span data-stu-id="70773-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="70773-109">您的應用程式必須配置 **ICINFO** 結構的記憶體，並在 **ICGetInfo** 中將指標傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="70773-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="70773-110">除非您的應用程式會搜尋特定的壓縮程式或解壓縮程式，否則 **ICINFO** 結構中的旗標會提供有關壓縮程式或解壓縮程式功能的最有用資訊。</span><span class="sxs-lookup"><span data-stu-id="70773-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="70773-111">若要取得預設的金鑰畫面播放速率和壓縮程式或解壓縮程式的預設品質值，您的應用程式可以傳送 [**icm \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) 和 [**icm \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) 訊息 (或使用 [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 和 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="70773-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="70773-112">若要判斷壓縮程式或解壓縮程式的最佳顯示格式，您的應用程式可以使用 [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) 函數。</span><span class="sxs-lookup"><span data-stu-id="70773-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="70773-113">若要判斷壓縮程式或解壓縮程式是否可以顯示 [關於] 對話方塊，請傳送訊息 (的 [**ICM \_**](icm-about.md) ，或使用 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="70773-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="70773-114">您也可以藉由傳送 \_ 關於訊息的 ICM、變更 *wParam* 參數的值 (或使用 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏) ，來顯示壓縮程式或解壓縮程式的 [關於] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="70773-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




