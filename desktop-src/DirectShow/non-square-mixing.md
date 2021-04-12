---
description: 非正方形混合
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: 非正方形混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510174"
---
# <a name="non-square-mixing"></a>非正方形混合

本主題適用于 Windows XP Service Pack 2 或更新版本。

當 VMR-9 混用兩個以上的資料流程時，有兩個點可進行調整：當混音器組合輸入資料流程時，以及配置器呈現者轉譯合成影像時。

![vmr 混合作業](images/vmr-nonsquare-mixing.png)

舊版的 VMR-9 一律會使用平方 (1:1) 圖元外觀比例 (PAR) 來組合輸入資料流程，即使只有一個影片串流也一樣。 如果輸入資料流程有非正方形圖元，這會導致不必要的調整作業。 當然應該盡可能避免調整，因為它會降低最終的影像品質。

從 Windows XP Service Pack 2 開始，VMR-9 支援兩種不同的方式來避免雙重調整的問題：

-   執行自訂配置器-展示者並支援 [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) 介面。
-   使用非方形混合模式。

本節說明非方形混合模式。 應用程式可以結合這兩種技術。

**非正方形混合的運作方式**

在非方形混合模式中，VMR-9 會選取一個輸入資料流程作為目標大小，也就是相等。 VMR 的混音器不會從該資料流程或任何其他影像大小相同的資料流程調整影片。 具有不同大小或外觀比例的資料流程會進行調整，以符合目標的等於和 letterboxed，以符合最終輸出影像的大小。

資料流程的選擇取決於目前的混合模式：

-   在 pin 0 上，會將 YUV 混合模式限制為一個影片串流。  (其他 pin 可能具有子圖片或隱藏式字幕資料流程。 ) 因此，VMR-9 一律會為目標映射大小和等於選取 pin 0。
-   在 RGB 混合模式中，VMR 會選取影像大小最大的資料流程。 如果有一個以上的，則會選取具有最高 z 順序的一個：如果仍然有系結，則會選取具有最低 pin 碼的串流。

**操作範例**

**範例1。** Stream 0 是 720 x 480 圖元，圖片的外觀比例為16:9。 Stream 1 是 640 x 480 圖元，圖片的外觀比例為4:3。

在此範例中，stream 0 具有最大的影像大小，因此無論是 RGB 混合模式或 YUB 混合模式，VMR 都會選擇此資料流程。 等於 32:27 (16:9/720:480) ，這表示影像必須以這個比例水準延展，以產生正確的16:9 圖片外觀比例。

為了符合目標，VMR 混音器會依據反向比率調整資料流程 1 (27:32) ，導致 540 x 480 影像。 這兩個數據流接著會合成至一個介面上。 若要正確顯示產生的影像，配置器展示者必須水準延展影像，以符合16:9 圖片的外觀比例。

![範例1。](images/vmr-nonsquare-mixing2.png)

**範例2。** Stream 0 是 720 x 480 圖元，圖片的外觀比例為16:9。 Stream 1 是 1024 x 768 圖元，圖片的外觀比例為4:3。

如果 VMR-9 使用 YUV 混合模式，它一律會選取資料流程0。 因此，它會將串流1延伸至 540 x 480 圖元，以符合資料流程0的 PAR。

如果 VMR-9 使用 RGB 混合模式，它會選取資料流程1做為目標，因為該資料流程具有最大的影像大小。 它會將資料流程0伸展為 1024 x 576 圖元的影像大小。 請注意，在此情況下，複合影像的大小為1:1，因此配置器呈現者不需要針對非正方形圖元進行修正。  (可能還是需要將影片延伸至目的地矩形的帳戶。 ) 

**使用非正方形混合模式**

如果下列任一條件成立，則建議使用非方形混合模式：

-   您的應用程式永遠不會將一個以上的影片串流傳送至 VMR-9。
-   您的應用程式會轉譯 DVD、電視或 ms dvr 檔案。 在此情況下，如果圖形硬體支援，您也應該使用 YUV 混合模式。

如果您的應用程式混合多個可能具有不同影像大小或圖元外觀比例的影片串流，建議使用預設的正方形混合模式。

若要設定非正方形混合模式，必須停止篩選圖形，並在 VMR-9 中斷所有輸入圖釘的連線。 然後使用 MixerPref9 NonSquareMixing 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ ：


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> 如果您將 MixerPref9 \_ NonSquareMixing 旗標與 MixerPref9 \_ ARAdjustXorY 旗標結合，VMR-9 會忽略 MixerPref9 \_ ARAdjustXorY 旗標。

 

如果您的應用程式使用具有非方形混合模式的自訂配置器提供者，請注意複合影像可能具有非平方的。 配置器-展示者必須將影像調整為平方 (1:1) 等同。

**靜態點陣圖**

如果您使用 [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) 介面將靜態點陣圖 blend 至影片，您應該將點陣圖視為第二個影片串流，以供 VMR 混合模式使用。

VMR 會將點陣圖視為等同于目標。 它不會縮放點陣圖以調整目標的圖元外觀比例。 在 VMR 的預設設定中，目標的1:1 等同于大部分的點陣圖。 在非方形混合模式中，目標可能具有非平方圖元。 為了確保點陣圖顯示正確，應用程式應該提供符合目標的影像。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



