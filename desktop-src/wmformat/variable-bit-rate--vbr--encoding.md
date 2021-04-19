---
title: 變數位速率 (VBR) 編碼
description: 變數位速率 (VBR) 編碼
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK，VBR 編碼
- 'Windows Media Format SDK，變數位元速率 (VBR) '
- Windows Media Format SDK，以品質為基礎的 VBR 編碼
- Windows Media Format SDK，未受限制的 VBR 編碼
- Windows Media Format SDK，受限的 VBR 編碼
- 編解碼器，VBR 編碼
- '編解碼器、變數位元速率 (VBR) '
- 編解碼器、以品質為基礎的 VBR 編碼
- 編解碼器，未受限制的 VBR 編碼
- 編解碼器，受限的 VBR 編碼
- 變數位元速率 (VBR) ，關於
- VBR (變數位速率) ，關於
- 以品質為基礎的 VBR 編碼，關於
- 未受限制的 VBR 編碼，關於
- 受限的 VBR 編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106990882"
---
# <a name="variable-bit-rate-vbr-encoding"></a>變數位速率 (VBR) 編碼

變數位元速率 (VBR) 編碼方式，是 (CBR) 的常數速率編碼的替代方式，而且有些編解碼器支援。 在 CBR 編碼的目的是維持編碼媒體的位元速率時，VBR 會致力於達到編碼媒體的最佳品質。

已編碼內容的品質取決於壓縮和解壓縮內容時遺失的資料量。 有許多因素在壓縮過程中會影響資料的流失量，但一般而言，原始資料越複雜且壓縮率越高，在壓縮過程中就會流失更多詳細資料。

有三種類型的 VBR 編碼：品質型、無限制且受限。

## <a name="quality-based-vbr-encoding"></a>以品質為基礎的 VBR 編碼

第一種類型的 VBR 編碼是以品質為基礎，它使用一種編碼傳遞。 以品質為基礎的 VBR 編碼可讓您指定數位媒體串流的品質層級，而不是位元速率。 然後，編解碼器會將內容編碼，讓所有範例都具有相當的品質。

以品質為基礎之 VBR 編碼的主要優點是，檔案中和從一個檔案到下一個檔案的品質都是一致的。 例如，您可以撰寫一個程式，從 CD 將歌曲複製到電腦上的 ASF 檔案。 在此情況下，一致的品質對終端使用者體驗而言可能比一致的檔案大小更重要。 使用以品質為基礎的 VBR 編碼，可確保複製的所有歌曲都具有相同的品質。

以品質為基礎之 VBR 編碼的缺點是，在編碼之前，沒有辦法知道編碼媒體的大小或頻寬需求。 這可以讓以品質為基礎的 VBR 編碼檔案不適用於記憶體或頻寬受限的情況，例如便攜媒體播放機或低頻寬的網際網路連線。

一般而言，以品質為基礎的 VBR 編碼非常適合本機播放或高頻寬的網路連接。 在這些情況下，一致的品質將提供更好的使用者體驗。

## <a name="unconstrained-vbr-encoding"></a>未受限制的 VBR 編碼

未受限制的 VBR 編碼會使用兩種編碼階段。 使用不受限制的 VBR 編碼時，您可以指定資料流程的位元速率，如同使用 CBR 編碼。 不過，編解碼器只會使用此值做為資料流程的平均位元速率，並進行編碼，讓品質盡可能高，同時維持平均。 編碼資料流程中任何時間點的實際位元速率可能會有極大的差異。

您未針對未受限制的 VBR 編碼設定緩衝區視窗，就像是針對 CBR 編碼的資料流程一樣。 相反地，編解碼器會根據編碼範例的需求來計算所需緩衝區視窗的大小。

未受限制的 VBR 編碼的優點在於壓縮的資料流程具有最高的可能品質，同時維持在可預測的平均頻寬內。

## <a name="constrained-vbr-encoding"></a>受限的 VBR 編碼

受限制的 VBR 編碼與未受限制的 VBR 編碼相同，不同之處在于您會在設定檔中指定最大位元速率和最大緩衝區視窗。 然後，編解碼器會使用最大值來決定壓縮資料的方式。 如果設定的最大值夠高，則受限制的 VBR 編碼將會產生與未受限制的 VBR 編碼相同的編碼資料流程。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**選擇編碼方法**](choosing-an-encoding-method.md)
</dt> <dt>

[**編解碼器功能**](codec-features.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**設定 VBR 資料流程**](configuring-vbr-streams.md)
</dt> <dt>

[**固定位元速率 (CBR) 編碼**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**雙通路編碼**](two-pass-encoding.md)
</dt> <dt>

[**使用 Two-Pass 編碼**](using-two-pass-encoding.md)
</dt> </dl>

 

 




