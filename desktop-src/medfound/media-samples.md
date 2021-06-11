---
description: 瞭解 Microsoft 媒體基礎中的媒體範例。 媒體範例是一個物件，其中包含零或多個緩衝區的已排序清單。
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: '媒體範例 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989153"
---
# <a name="media-samples-microsoft-media-foundation"></a>媒體範例 (Microsoft 媒體基礎) 

媒體範例是一個物件，其中包含零或多個緩衝區的已排序清單。 媒體範例會公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面。 一個範例中包含的資料量，取決於建立範例的元件，以及緩衝區中的資料類型。 針對未壓縮的影片，範例通常會保留單一的影片畫面。 若是未壓縮的音訊，資料量可能會有所不同，但通常音訊框架不會跨越兩個樣本。 針對壓縮的資料，可能不適用這些指導方針。

基於效率的原因，單一範例可能包含多個緩衝區。 例如，在 ASF 檔案中，影片框架通常會分散在多個 ASF 封包中。 媒體來源可能會將封包讀取至多個緩衝區。 來源只會將所有緩衝區放入一個範例中，而不是將每個片段複製到一個緩衝區。 下游元件接著可以決定是否要將較小的緩衝區複製到一個連續的緩衝區。 一般而言，如果您要撰寫管線元件，則應該假設任何範例可能包含一個以上的緩衝區。

此章節包含下列主題。



| 主題                                                        | 描述                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [使用媒體範例](working-with-media-samples.md) | 描述媒體範例的一般行為。                                                                         |
| [影片範例](video-samples.md)                           | 描述專門針對用來保存未壓縮影片畫面的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 執行。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體緩衝區](media-buffers.md)
</dt> <dt>

[媒體基礎基本](media-foundation-primitives.md)
</dt> </dl>

 

 



