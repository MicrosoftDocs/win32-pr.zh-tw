---
title: 固定位元速率 (CBR) 編碼
description: 固定位元速率 (CBR) 編碼
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK，CBR 編碼
- 'Windows Media Format SDK，常數位元速率 (CBR) '
- 編解碼器，CBR 編碼
- '編解碼器、常數速率 (CBR) '
- '固定位元速率 (CBR) '
- 'CBR (常數位速率) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372539"
---
# <a name="constant-bit-rate-cbr-encoding"></a>固定位元速率 (CBR) 編碼

常數位速率 (CBR) 編碼是 Windows Media Format SDK 的預設編碼方法。 使用 CBR 編碼時，您會指定資料流程的目標位速率，且編解碼器會使用所需的壓縮數量來達成。

在編碼之前，使用 CBR 編碼，編碼資料流程的位元速率和大小都是已知的。 例如，如果您要將三分鐘的歌曲編碼成每秒32000位，您知道檔案大小大約是 704 kb (32000 bps x 180 秒/8 位/每個位元組/1024) 。 您也知道串流編碼內容所需的頻寬大約是每秒32000位。

下一節所述的限制變數位速率編碼 () 也可讓您知道編碼之前的位元速率，但由於速率是變數，因此產生的檔案無法有效率地串流處理為在 CBR 模式中編碼的檔案。 使用 CBR 時，一段時間的位元速率永遠保持接近平均或目標位元速率，而且可以指定變異數。

CBR 編碼的缺點是編碼內容的品質不會是常數。 因為有些內容較難壓縮，所以 CBR 串流的部分會比其他部分的品質低。 例如，典型的電影有一些相當靜態的場景，以及一些完全行動的場景。 如果您使用 CBR 將電影編碼、靜態的場景，因此可以有效率地編碼，則其品質會比動作場景高，更難以有效率地編碼。

CBR 編碼也可能導致不一致的品質從某個檔案到另一個檔案。 如果您使用 CBR 以相同的位元速率來編碼數個不同內容的歌曲，您可能會注意到兩者之間的品質有一些差異。

一般而言，CBR 檔案品質的變化會以較低的位元速率更明顯。 以較高的位元速率來說，CBR 編碼檔案的品質仍會有所不同，但對使用者而言，品質問題將會比較不明顯。 使用 CBR 編碼時，您應該在傳遞案例允許的情況下設定最高的頻寬。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**選擇編碼方法**](choosing-an-encoding-method.md)
</dt> <dt>

[**編解碼器功能**](codec-features.md)
</dt> <dt>

[**變數位速率 (VBR) 編碼**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




