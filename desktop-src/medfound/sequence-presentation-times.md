---
description: 本主題描述 Sequencer 來源如何處理播放期間的呈現時間。
ms.assetid: 0d095e25-5ccf-4319-8767-07b417ed7ee8
title: 順序呈現時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45ea9c8b315171365810f33bb9a66ca4d223fb2119d7aea19288c3ebdd93ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238364"
---
# <a name="sequence-presentation-times"></a>順序呈現時間

本主題描述 [Sequencer 來源](sequencer-source.md) 如何處理播放期間的呈現時間。

## <a name="overview"></a>概觀

Sequencer 來源支援兩種不同的模式：播放清單順序和編輯順序。

在編輯順序中，應用程式會在開始播放之前，事先指定每個區段的持續時間。 在播放清單順序中，應用程式不會事先指定持續時間。  (事實上，可能不知道持續時間。 ) 

在這兩種情況下，您都可以指定區段的媒體開始和媒體停止時間。 這些時間會指定來源檔案中區段開始和結束的位置。 例如，假設原始程式檔的長度是90秒。 如果您想要修剪前10秒和最後10秒，您需要指定下列值：

-   媒體啟動：10秒
-   媒體停止：80秒

若要指定媒體開始時間，請在來源節點上設定 [ [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) ] 屬性。 若要指定媒體停止時間，請在來源節點上設定 [ [MF \_ TOPONODE \_ MEDIASTOP](mf-toponode-mediastop-attribute.md) ] 屬性。

若要建立編輯順序，請在建立媒體會話時設定 [ [MF \_ 會話 \_ 全域 \_ 時間](mf-session-global-time-attribute.md) ] 屬性。 否則，媒體會話會預期播放清單順序。 在編輯順序中，每個區段拓撲都必須有 [mf \_ 拓撲 \_ PROJECTSTART](mf-topology-projectstart-attribute.md) 屬性和 [mf \_ 拓撲 \_ PROJECTSTOP](mf-topology-projectstop-attribute.md) 屬性。

## <a name="playlist-sequences"></a>播放清單順序

在播放清單順序中，標記法會從零開始，並在區段界限之間繼續。 原生來源會提供時間戳記等於媒體時間的範例。 管線會將時間戳記轉換為正確的呈現時間，如下所示：

-   新的時間戳記 = 媒體時間 + 位移−媒體開始

*Offset* 的值是前一個區段結束的呈現時間。 若為第一個區段，則位移為零。 以下是計算這些時間戳記轉換的兩個範例：

-   範例1：假設第一個區段 (S1) 的長度為10秒，而第二個區段 (S2) 具有媒體開始時間為零。 原生來源使用媒體時間作為時間戳記，因此 S2 的第一個範例的時間戳記為零。 位移是 (S1) 的持續時間為10秒，因此調整的時間戳記為： 0 + 10 − 0 = 10 秒。
-   範例2：假設區段 S1 的長度為10秒，而 S2 的媒體開始時間為5秒。 S2 的第一個範例有5秒的時間戳記 (媒體時間) 。 位移為10秒，因此調整的時間戳記為： 5 + 10 − 5 = 10 秒。

來源節點下游的所有管線元件都會收到範例，其中包含已調整的時間戳記。 拓撲中的來源節點可能會有不同的媒體開始時間，因此會針對拓撲的每個分支分別計算其調整。

當簡報切換至下一個區段時，標記法的時鐘不會停止或重設，而且呈現時間會以單純方式遞增。 在新的區段開始之前，媒體會話會將 [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) 事件傳送給應用程式。 事件會指定區段的開始時間（相對於呈現時鐘）和位移的值。 當新的區段開始時，管線會[](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)呼叫以 VT 空白值的 Sequencer 來源開始 \_ 。 Sequencer 來源傳送的 [MESourceStarted](mesourcestarted.md) 事件沒有開始時間。

若要搜尋，應用程式會指定區段識別碼加上區段內的時間位移。 搜尋之後，簡報時鐘就會從 *區段* 位移開始。 以下是該程式如何運作的範例：

-   範例3：應用程式會搜尋分割 S3，其區段位移為10秒。 簡報時鐘的開始時間為10秒， (區段位移) 。 位移不包含區段 S1 和 S2 的持續時間。 Sequencer 來源傳送的 [MESourceStarted](mesourcestarted.md) 事件，其開始時間等於區段位移10秒。

搜尋之後，如果播放繼續前往下一個區段，則轉換的運作方式就如同先前的範例，差別在於位移不包含略過的區段。

以下是一些進一步的詳細資料，會影響取樣的時間戳記：

-   您可能需要在媒體停止時間以外的時間進行的資料。 管線會從來源提取所需的資料量，然後修剪該解碼器的輸出範例。
-   轉換可能會緩衝資料。 例如，音訊效果可能需要這樣做。 當區段結束時，轉換的最後一個樣本上的時間戳記會早于區段的結尾，因為轉換會保留一些資料。 當下一個區段開始時，第一個樣本上的時間戳記會稍微早于區段的起點。 時間戳記中沒有間距，所以到達媒體接收器的資料是連續的。 當最後一個區段結束時，管線會清空轉換，因此不會遺失任何資料。
-   來源可能必須稍微早于媒體開始時間，才能挑選先前的主要畫面格。 因此，在調整之後，第一個範例可能會有負面的呈現時間。

## <a name="editing-sequences"></a>編輯順序

在編輯順序中，應用程式會藉由設定 [**mf \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 和 [**mf \_ 拓撲 \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) 屬性，預先指定區段界限。 管線會計算時間戳記的調整，與播放清單順序的方式幾乎相同：

-   針對位移，它會使用 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md)的值，而不是使用區段觀察到的結尾。

-   針對搜尋，位移會使用等於區段的 [**MF \_ 拓撲 \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) 值加上區段位移的值。

因此，即使應用程式搜尋至另一個區段，編輯順序中的呈現時間一律會相對於簡報的開頭。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 



