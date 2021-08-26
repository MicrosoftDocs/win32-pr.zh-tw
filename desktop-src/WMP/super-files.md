---
title: Super 檔案
description: Super 檔案
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player行動外觀、美工檔案
- 外觀、美工檔案
- 適用于外觀、藝術的檔案
- 適用于面板的美工圖案、超級檔案檔案
- Windows Media Player行動外觀、超級檔案檔案
- 外觀，超級檔
- 外觀中的超級檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbd6734e0491b5fc0e6552db14b3c0ab4489e466e7851ef4b474e84d2d85183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122860"
---
# <a name="super-files"></a>Super 檔案

Super 檔案是用來儲存已停用的 trackbars 映射。 由於主要的 [顯示檔] 影像會顯示在背景檔案中，而使用者可點擊 thumb 影像，而不是 [顯示] 影像，因此 trackbars 只需要停用的影像。 它會儲存在面板定義檔的點陣圖區段中，由 Super 所定義的檔案中。 超級檔案也可以針對其他按鈕（例如靜音）儲存已推送和停用的影像，而不需要是點擊類型按鈕。

> [!Note]  
> 在 Windows Media Player 10 行動版或更新版本的外觀中不會使用最新的檔，因為搜尋 trackbars 的已停用影像位於 seekthumb 檔案中。

 

下圖是一般的超級檔案。

![super 檔案](images/cesdksup.png)

這會儲存已停用的 trackbars 影像和靜音按鈕。 這些影像是依點陣圖區段所定義的位移。

已停用的 [已停用的檔] 影像的背景區域，與背景檔案中的對應區域完全相符。 這點很重要，因為針對已停用的 [檢視器] 影像定義的整個矩形將會取代背景檔案中的相符區域。 這可確保停用的 [貼幅] 影像可順暢地混合到背景影像。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**美工檔案**](art-files-mobile.md)
</dt> </dl>

 

 




