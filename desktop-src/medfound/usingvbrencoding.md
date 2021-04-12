---
description: 本節說明如何設定 VBR 資料流程。
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: '使用 VBR 編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191746"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>使用 VBR 編碼 (Microsoft 媒體基礎) 

如 [編碼方法](encodingmethods.md) 主題中所述， (VBR) 編碼的變動位元速率，以改善內容品質的一致性。 您可以用相同的方式來設定 VBR 資料流程， (CBR) 資料流程，但緩衝區參數 (位元速率和緩衝區視窗) 。 本節說明如何設定 VBR 資料流程。

## <a name="configuring-quality-based-vbr"></a>設定以品質為基礎的 VBR

使用以品質為基礎的 VBR 方法進行編碼並不需要任何預先定義的緩衝區參數。 相反地，您可以指定品質層級 (從0到 100) ，編碼器會使用此層級來動態判斷適當的緩衝區參數。 此編碼模式只會使用一次編碼。

您可以列舉音訊編解碼器的支援品質型 VBR 輸出類型。 設定輸出型別時，您必須使用 SQL-DMO 所傳回的其中一個類型。 如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。

若要設定品質型的 VBR 影片資料流程，您必須設定下表所列的屬性。



| 屬性                                            | 描述                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | 設定為 VARIANT \_ TRUE。                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | 設定為所需的品質值，從0到100。 並非所有品質值都代表不同的設定。 如需詳細資訊，請參閱屬性描述。 |



 

## <a name="configuring-unconstrained-vbr"></a>設定未受限制的 VBR

未受限制的 VBR 編碼可讓編碼器在沒有任何明確緩衝區限制的情況下，變更個別樣本的大小。 不過，產生的內容期間的平均位元速率必須小於或等於指定的值。 未受限制的 VBR 需要兩次編碼階段。

您可以列舉音訊編解碼器支援的雙通路 VBR 輸出類型。 設定輸出型別時，您必須使用 SQL-DMO 所傳回的其中一個類型。 如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。

若要設定未受限制的 VBR 影片資料流程，您必須設定下表所列的屬性。



| 屬性                                            | 描述                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | 設定為 VARIANT \_ TRUE。                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | 設定為2。                            |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | 設定為所需的平均位元速率。 |



 

## <a name="configuring-peak-constrained-vbr"></a>設定 Peak-Constrained VBR

尖峰限制的 VBR 就像是不受限制的 VBR，因為它會限制為數據流持續時間的平均位元速率。 此外，尖峰限制的 VBR 會符合尖峰緩衝區。 這個緩衝區是使用尖峰位元速率和尖峰緩衝區視窗來描述，就像是平均位元速率和緩衝區視窗描述的 CBR 緩衝區一樣。 這種模式可讓編碼器在編碼個別樣本的方式上有彈性，同時遵守尖峰限制。 當解碼是由裝置中的晶片（例如 DVD 播放機）執行時，這項功能特別有用，其中有必須考慮的硬體限制。

支援的尖峰型、VBR 音訊編碼器輸出類型與針對未受限制的 VBR 列舉的類型相同。 設定此的尖峰值，並使用傳遞的類型。 如需詳細資訊，請參閱 [列舉特定編碼模式的音訊類型](enumeratingaudiotypesforspecificencodingmodes.md)。

若要設定尖峰限制的 VBR 影片資料流程，您必須使用 **IPropertyBag：： Write** 方法來設定下表中所列的屬性。



| 屬性                                            | 描述                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | 設定為 VARIANT \_ TRUE。                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | 設定為2。                                                       |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | 設定為所需的平均位元速率。                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | 設定為所需的尖峰位元速率。                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | 設定為對應至尖峰位速率的緩衝區視窗。 |



 

> [!Note]  
> 建議您將尖峰位速率設定為至少兩倍的平均位元速率。 將尖峰速率設定為較低的值，可能會造成編解碼器將內容編碼為雙向 CBR，而不是尖峰限制的 VBR。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> <dt>

[使用 Two-Pass 編碼](usingtwoencodingpasses.md)
</dt> <dt>

[使用音訊](workingwithaudio.md)
</dt> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 



