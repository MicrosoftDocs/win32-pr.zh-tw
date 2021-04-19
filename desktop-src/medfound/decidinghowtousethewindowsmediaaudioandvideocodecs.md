---
description: 使用編解碼器和 DSP 物件
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: 使用編解碼器和 DSP 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981741"
---
# <a name="using-the-codec-and-dsp-objects"></a>使用編解碼器和 DSP 物件

有幾種方式可使用 Windows Media 音訊和影片編解碼器和 Dsp 來編碼、解碼或轉換您的數位媒體內容。 Windows Media 音訊和影片編解碼器和 DSP API 適用于需要手動設定編解碼器和 DSP 物件的使用者，或在 Windows Media Sdk （例如 Windows Media Format SDK 或媒體基礎 SDK）之外的內容之外使用它們。

內容建立者和終端使用者可以使用各種工具和應用程式來編碼 Windows Media 音訊或 Windows Media 視訊串流中的內容。 例如，Windows Media 編碼器的設計目的是要讓編碼程式更簡單。 同樣地，Windows Media Player 是特別設計來與以 Windows Media 格式編碼的數位媒體資料搭配運作。 針對許多應用程式，使用 Windows Media 編碼器 SDK 或 Windows Media Player SDK 都是必要的。 特別是，這兩項技術適用于類似其自動化工具功能的案例。

如果您需要更充分掌控編碼或解碼程式，但仍想使用 Advanced Systems 格式 (ASF) 作為媒體資料的容器，Windows Media Format SDK 可能是不錯的選擇。 Windows Media Format SDK 的物件提供彈性的架構來建立 ASF 檔案，並提供 Windows Media 音訊和 Video 編解碼器的內建支援。

媒體基礎 SDK 是 Windows Vista 的新功能，藉由提供可自訂的媒體管線，大幅簡化編碼和解碼。 您可以設定輸入和輸出媒體屬性，媒體基礎拓撲載入器會為您設定必要的編解碼器和 Dsp。

直接使用編解碼器物件的主要原因是要在 ASF 容器之外使用 Windows Media 音訊和影片編解碼器。 使用編解碼器和 DSP 物件也提供使用任何更抽象技術無法使用的控制層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 



