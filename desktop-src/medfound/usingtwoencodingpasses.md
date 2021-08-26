---
description: 雙通編碼可用於常數位元速率 (CBR) 和變數位元速率 (VBR) 編碼與某些 Windows 媒體編解碼器。
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: '使用 Two-Pass 編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a79678e3b4396dfe87b93dfda7c9fd26487b8fdba83d2214509675ee742951
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887108"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>使用 Two-Pass 編碼 (Microsoft 媒體基礎) 

雙通編碼可用於常數位元速率 (CBR) 和變數位元速率 (VBR) 編碼與某些 Windows 媒體編解碼器。 您可以藉由抓取 [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) 屬性，找到編解碼器所支援的最大編碼傳遞數目。 所有編解碼器皆不支援兩個以上的傳遞。 將[MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md)屬性設定為2，以將 DMO 設定為使用兩個階段。

將範例一次傳遞給編碼器 DMO 一次，就像在單一階段模式中一樣。 當您處理前置處理行程的輸入範例時，對 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) 或 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 的呼叫會傳回 **\_ FALSE**，表示不會產生任何輸出。

在第一) 次傳遞 (的最後一個輸入第一次處理之後，您必須設定 [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) 屬性，以通知編解碼器下一個輸入所處理的是第二次的輸入。 這個屬性不需要任何值，因此您應該使用空白的 **VARIANT** 結構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 
