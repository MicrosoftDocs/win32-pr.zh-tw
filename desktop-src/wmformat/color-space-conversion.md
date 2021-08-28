---
title: 色彩空間轉換
description: 色彩空間轉換
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows媒體格式 SDK，色彩空間轉換
- Advanced Systems Format (ASF) 、色彩空間轉換
- ASF (Advanced Systems Format) ，色彩空間轉換
- 色彩空間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23b596b7ae8ed32e64cc3ebe8a23f1bc52dafb5304308104aba083675afe6370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447938"
---
# <a name="color-space-conversion"></a>色彩空間轉換

在設定檔和輸入格式中，壓縮影片格式的色彩深度通常會有差異。 發生這種情況時，來源影片必須轉換成符合目的地的色彩空間。 寫入器會處理這個進程，並與內部的色彩空間轉換器進行通訊。

讀取器也會與色彩空間轉換器通訊，以協調壓縮格式和輸出格式之間的任何差異。

如同在資料上執行的所有轉換，在色彩深度之間轉換可以減少輸出品質。 可能的話，您應該使用具有與壓縮格式相同色彩深度的輸入和輸出格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**檔案寫入功能**](file-writing-features.md)
</dt> <dt>

[**使用輸入**](working-with-inputs.md)
</dt> <dt>

[**使用輸出**](working-with-outputs.md)
</dt> </dl>

 

 




