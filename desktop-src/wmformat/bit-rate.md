---
title: 位元速度
description: 位元速度
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows媒體格式 SDK，位元速率
- Advanced Systems Format (ASF) ，bit 速率
- ASF (Advanced Systems Format) ，bit 速率
- 位元速率，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a15332e18d47a72974098ad38c6a942ceaf4780e1b79dffacd49382e3416ae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809868"
---
# <a name="bit-rate"></a>位元速度

位元速率指的是從 ASF 檔案傳遞的每秒資料量。 位元速率測量的單位為每秒 (bps) 或每秒千位 (Kbps) 。 位元速率通常會與頻寬混淆，這是網路資料傳輸容量的度量。 頻寬也是以 bps 和 Kbps 來測量。

Windows 媒體格式 SDK 可以用來建立應用程式，以從網際網路或內部網路位置傳遞串流 Windows 媒體內容。 當您在網路或網際網路上串流處理資料時，位元速率對終端使用者體驗而言相當重要。 如果網路可用的頻寬小於 ASF 檔案的位元速率，檔案的播放將會以某種方式中斷。 通常，頻寬不足會導致略過兩個樣本，或在多個資料經過緩衝處理時暫停播放。

在建立時，系統會根據所用設定檔中包含的資料流程類型和數目，在建立時指派每個 ASF 檔案的位元速率值。 個別的串流有自己的位元速率。 位速率可以是固定的 (原始資料會以接近相同速率的平均資料量) 或變數的方式來進行壓縮， (原始資料會以平均維持相同品質的方式進行壓縮，即使這可能表示) 不平均的資料流程。 不同的位速率類型可以套用至相同檔案中的不同資料流程。

您可以針對數個不同的資料流程編碼相同的內容，每個資料流程各有不同的位元速率。 然後您可以設定資料流程，讓它們彼此互斥。 這可讓您建立單一檔案，以串流處理至具有不同頻寬的使用者。 這項功能稱為「多位元率」或「MBR」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](concepts.md)
</dt> <dt>

[**固定位元速率 (CBR) 編碼**](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[**輸入、串流和輸出**](inputs-streams-and-outputs.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> <dt>

[**變數位速率 (VBR) 編碼**](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




