---
title: 提供消費者介面
description: 提供消費者介面
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player 外掛程式、屬性頁
- 外掛程式，屬性頁
- 數位信號處理外掛程式，屬性頁
- DSP 外掛程式、屬性頁
- 數位信號處理外掛程式，使用者介面
- DSP 外掛程式，使用者介面
- 屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183913"
---
# <a name="providing-a-user-interface"></a>提供消費者介面

DSP 外掛程式可以提供屬性頁來建立使用者介面。 若要這樣做，外掛程式必須包含可提供 **IPropertyPage** 介面執行的屬性頁物件。 DSP 外掛程式物件必須執行 **ISpecifyPropertyPages：： GetPages**，以允許 Windows Media Player 找出並識別外掛程式的正確屬性頁。

**顯示狀態圖形**

DSP 外掛程式可在 [Windows Media Player 狀態] 區域中顯示一小圖形或圖形系列，以通知使用者外掛程式為使用中狀態。 若要支援這項功能，外掛程式必須執行 **IPropertyBag** 介面。 Windows Media Player 會呼叫 **IPropertyBag：： Read**，提供要求的屬性名稱 "IconStreams" 的指標，該名稱會區分大小寫，而 **VARIANT** 結構的指標則會接收圖形的資料。 如果有多個圖形) ，外掛程式會建立 **istream** 物件 (或 **ISTREAM** 物件的 SAFEARRAY，然後將圖形資料（包括標頭資訊）載入至資料流程，然後使用 **VARIANT** 結構的 **punkVal** 成員傳回 **istream** 物件的指標。 如果外掛程式只提供一個圖形，則會將 **VARIANT** 結構的 **vt** 成員指定為 vt \_ UNKNOWN。 如果外掛程式使用 SAFEARRAY 來提供多個圖形 **IStream** 物件，它會將 **VARIANT** 結構的 **vt** 成員指定為 vt \_ 陣列。

圖形可以用各種不同的檔案格式儲存，包括：

**BMP**

Microsoft Windows 點陣圖影像未壓縮。

**JPEG**

通常用於網頁的壓縮影像格式。 JPEG 格式檔案的副檔名通常為 .jpg。

**GIF**

通常用於網頁的壓縮影像格式。

**PNG**

通常用於網頁的壓縮影像格式。

DSP 外掛程式圖形的大小上限為38圖元寬和14圖元高。

包含狀態圖形的 **IStream** 位元組資料流程必須包含標頭資訊。 如果沒有標頭資訊，Windows Media Player 無法正確地識別圖形的類型，因此不會載入影像。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DSP 外掛程式開發人員總覽**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




