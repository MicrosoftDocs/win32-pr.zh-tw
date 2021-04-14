---
title: 取得壓縮機和 Decompressors 的相關資訊
description: 取得壓縮機和 Decompressors 的相關資訊
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，取得有關壓縮機的資訊
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，取得有關壓縮機的資訊
- ICGetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371971"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a><span data-ttu-id="9e1da-106">取得壓縮機和 Decompressors 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="9e1da-106">Obtaining Information About Compressors and Decompressors</span></span>

<span data-ttu-id="9e1da-107">下列範例會使用 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數來取得有關壓縮或解壓縮的資訊。</span><span class="sxs-lookup"><span data-stu-id="9e1da-107">The following example uses the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function to obtain information about a compressor or decompressor.</span></span>


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



<span data-ttu-id="9e1da-108">下列範例會使用 [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 和 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏來取得預設值。</span><span class="sxs-lookup"><span data-stu-id="9e1da-108">The following example uses the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros to obtain the default values.</span></span>


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



<span data-ttu-id="9e1da-109">下列範例會使用 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 和 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏來顯示壓縮程式或解壓縮程式的 [關於] 對話方塊（如果對話方塊存在的話）。</span><span class="sxs-lookup"><span data-stu-id="9e1da-109">The following example uses the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) and [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macros to display an About dialog box for the compressor or decompressor, if the dialog box exists.</span></span>


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




