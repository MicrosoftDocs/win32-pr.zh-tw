---
description: ASF 編碼類型
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: ASF 編碼類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111892"
---
# <a name="asf-encoding-types"></a>ASF 編碼類型

編碼方法全都專注于編碼器所使用的緩衝區，以管理未壓縮的輸入資料。 這個緩衝區是以資料流程的位元速率（每秒位數）和緩衝區視窗（以毫秒為單位）來定義。 編碼為 ASF 檔案時，Windows Media 編碼器會遵守緩衝區的限制。 如需有關緩衝區視窗的詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。 瞭解每個方法的使用方式和時機，可以協助您建立高品質的壓縮內容。 下表包含每個可用編碼方法的相關主題連結，可供應用程式用來將媒體資料編碼為 ASF。



| 編碼方法                                                                                      | Description                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [常數位元速率編碼](constant-bit-rate-encoding.md)                                         | 編碼器會將資料壓縮成指定的位元速率。                                                                                                                                                     |
| [以品質為基礎的變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)       | 編碼器會將資料壓縮成特定的品質值，讓編碼媒體的品質在整個持續期間都一致，不論產生的資料流程是否有緩衝區需求。 |
| [不受限制的變數位速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)       | 編碼器會將資料壓縮成可能的最高品質，同時維持指定的位元速率。 這種模式也稱為2傳遞變數位元速率 (VBR) 編碼。                                    |
| [尖峰限制的可變位速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md) | 編碼器會將資料壓縮成指定的位元速率，同時將緩衝區值保留在指定的最大緩衝區視窗和位元速率。 這種模式也稱為雙通路尖峰的 VBR。                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> </dl>

 

 



