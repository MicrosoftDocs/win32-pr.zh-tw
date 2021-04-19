---
description: Windows Media Center Edition 的解碼器設定
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Windows Media Center Edition 的解碼器設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975599"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Windows Media Center Edition 的解碼器設定

Windows XP Media Center Edition 2005 和更新版本會使用 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面來設定音訊解碼篩選器，以進行電視和 DVD 播放。 以下是支援的屬性。



| 屬性 GUID                   | Description                                      |
|---------------------------------|--------------------------------------------------|
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式 | 設定音訊輸出格式。 請參閱＜備註＞。 |



 

## <a name="remarks"></a>備註

CODECAPI \_ 音訊 \_ 輸出格式屬性的值 \_ 是 GUID 的字串表示，儲存為 **BSTR** 值。 定義了下列 Guid。



| GUID                                                        | Description                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 身歷聲 \_ MATRIXENCODED | 軟體音訊篩選器應該執行軟體解碼並輸出身歷聲音訊串流，並將多頻道音訊矩陣編碼為兩個通道。                                                   |
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 身歷聲                | 軟體音訊篩選器應該執行軟體解碼並輸出身歷聲音訊串流。                                                                                                                   |
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式的 \_ SPDIF \_ PCM                 | 軟體音訊篩選器應該執行軟體音訊解碼，雖然電腦的實體輸出可能是數位介面，例如 S/PDIF。                                                      |
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式的 \_ SPDIF \_ 位流           | 軟體音訊篩選器不應該執行軟體音訊解碼，但應該透過連接到數位音訊連結的裝置（例如 S/PDIF），傳遞原始數位音訊位流進行外部處理。 |
| CODECAPI \_ 音訊 \_ 輸出 \_ 格式 \_ PCM \_ 耳機            | 軟體音訊篩選器應該執行軟體音訊解碼，並且應該套用專屬處理以針對耳機進行優化。 這項設定的支援是選擇性的。                                     |



 

> [!Note]  
> **ICodecAPI** 介面會將編解碼器屬性儲存為索引鍵/值組，其中索引鍵是 GUID，而值則是 **VARIANT** 型別。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼器和解碼器開發](encoder-and-decoder-development.md)
</dt> </dl>

 

 



