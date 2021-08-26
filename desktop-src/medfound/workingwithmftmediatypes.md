---
description: 使用 MFT 媒體類型
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: 使用 MFT 媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ead31c4291cf41cff62f4341227bf0ee1ad22d12e96a6c9eff87ff5a3e6faa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886948"
---
# <a name="working-with-mft-media-types"></a>使用 MFT 媒體類型

媒體類型是描述媒體資料流程格式的方式。 在媒體基礎中，媒體類型會以 **IMFMediaType** 介面表示。 這個介面會繼承 **IMFAttributes** 介面。 媒體類型的詳細資料會指定為屬性。

若要建立新的媒體類型，請呼叫 **MFCreateMediaType** 函數。 此函數會傳回 **IMFMediaType** 介面的指標。 媒體類型一開始沒有任何屬性。

媒體基礎 SDK 提供數個協助程式函式，可從格式結構初始化媒體類型。 例如，函式 **MFInitMediaTypeFromVideoInfoHeader** 會從 **VIDEOINFOHEADER** 結構初始化影片類型，而函數 **MFInitMediaTypeFromWaveFormatEx** 會從 **WAVEFORMATEX** 或 **WAVEFORMATEXTENSIBLE** 結構初始化影片類型。

編解碼器所使用的格式類型通常會限制為 **VIDEOINFOHEADER** 和 **WAVEFORMATEX** 結構所描述的格式類型。

如需有關建立及存取媒體基礎媒體類型的詳細資訊，請參閱媒體基礎 SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用編解碼器 MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



