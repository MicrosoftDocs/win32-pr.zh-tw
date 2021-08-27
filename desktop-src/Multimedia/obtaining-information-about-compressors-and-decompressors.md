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
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038438"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>取得壓縮機和 Decompressors 的相關資訊

下列範例會使用 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數來取得有關壓縮或解壓縮的資訊。


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



下列範例會使用 [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 和 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏來取得預設值。


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



下列範例會使用 [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) 和 [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) 宏來顯示壓縮程式或解壓縮程式的 [關於] 對話方塊（如果對話方塊存在的話）。


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




