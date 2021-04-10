---
title: 色彩空間轉換
description: 色彩空間轉換
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK，色彩空間轉換
- Advanced Systems Format (ASF) 、色彩空間轉換
- ASF (Advanced Systems Format) ，色彩空間轉換
- 色彩空間轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183495"
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

 

 




