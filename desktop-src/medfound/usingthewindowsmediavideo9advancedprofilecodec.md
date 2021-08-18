---
description: 使用 Windows Media 視訊 9 Advanced Profile
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: 使用 Windows Media 視訊 9 Advanced Profile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258c32f14d1a7a42e1450c8265e2a611bd17b3b92b98f5433c93b91251e299c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012168"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>使用 Windows Media 視訊 9 Advanced Profile

「使用[影片](workingwithvideo.md)」一節中所述的基本影片程式也直接套用到 Windows Media 視訊 9 Advanced Profile。 不需要任何特殊程式。

Windows Media 視訊 9 Advanced Profile 與類別識別碼 CLSID \_ CWMV9EncMediaObject 和 clsid CWMVDecMediaObject 相關聯 \_ 。 使用此編解碼器之媒體類型的 FOURCC 值為 "WVC1"。

Windows Media 視訊 9 Advanced Profile 支援所有常見的編碼模式，以及交錯編碼、混合交錯和漸進編碼、與顯示不同的解析度，以及範圍縮減功能。 另一項功能是在位資料流程本身儲存序列和框架中繼資料的能力;之前，這必須使用 ASF 和資料單位延伸 API。

您可以使用登錄設定來控制 Windows Media 視訊 9 Advanced Profile 的下列屬性，而且沒有對應的 **IPropertyBag** 或 **IPropertyStore** 字串：

-   Dquant 選項。
-   Dquant 強度。
-   強制重迭。
-   動作向量成本方法。

## <a name="achieving-optimal-visual-quality"></a>達到最佳的視覺品質

針對大部分的影片資料，若要使用 Windows Media 視訊 9 Advanced Profile 達成最佳的視覺品質，您可以將[MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md)屬性設定為1。

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>關於先前的 Windows Media 視訊 9 Advanced Profile 編解碼器

Windows Media 視訊 9 advanced profile 編解碼器的最新版本是以「運動」圖片和電視工程師為基礎， (適用于 VC-1 (smpte 421M) Advanced Profile 的) 標準。 此編解碼器會取代 Windows 的舊版編解碼器，也稱為 Windows Media 視訊 9 Advanced Profile 編解碼器（由 FOURCC 碼 "WMVA" 識別）。 前一版的 VC-1 編解碼器是在 VC-1 advanced profile standard 完成之前執行，不再支援。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片](workingwithvideo.md)
</dt> 
<dt>

[使用 Windows Media 視訊 9 advanced Profile 編解碼器的 advanced 設定](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



