---
title: 產生非標準格式
description: 產生非標準格式
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- 音訊壓縮管理員 (的) 、非標準格式
- " (的音效壓縮管理員) 、非標準格式"
- 未通過範例，非標準格式
- acmFormatSuggest 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839932"
---
# <a name="generating-a-nonstandard-format"></a>產生非標準格式

有時候應用程式需要非標準的格式。 例如，應用程式可能需要 16 kHz 的 ADPCM 格式檔案。 因為 16 kHz 並非標準的，所以列舉函數不會產生此格式。 事實上，在應用程式中撰寫格式演算法的自訂程式碼很簡單，沒有可靠的方式可以產生非標準格式。 不過，有時可能會藉由使用所有必要的資訊設定有效的 PCM 格式，然後使用 [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) 函式，來產生類似的格式。 因為壓縮機和 decompressors 會嘗試建議最接近所需格式的格式，所以通常會保留通道數目和頻率。

 

 




