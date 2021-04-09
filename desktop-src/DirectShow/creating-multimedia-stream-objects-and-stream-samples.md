---
description: 建立多媒體資料流程物件和資料流程範例
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: 建立多媒體資料流程物件和資料流程範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945662"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>建立多媒體資料流程物件和資料流程範例

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

支援 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 介面的物件是多媒體資料流程的基本容器。 **IMultiMediaStream** 介面包含列舉物件之資料流程的方法;這些資料流程通常是影片和音訊資料，但可包含任何格式的資料，例如隱藏式字幕、純文字或 SMPTE 時間碼。 但是， **IMultiMediaStream** 介面是泛型容器，開發人員可以建立其他版本的介面，以支援特定的資料格式。 例如，執行 [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) 介面的物件可以列舉及控制任何 DirectShow 資料格式的資料流程。 由於個別資料流程的格式是特定的，因此，它們至少支援兩個不同的介面：一個泛型和一個資料特有的。 每個資料流程都支援 [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) 介面，這會提供方法來取出其格式以及資料流程本身的指標。 相反地， [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) 介面具有處理轉譯影片資料的方法。 任何衍生自 **IMultiMediaStream** 的介面也支援建立資料流程範例，也就是串流資料的基本單位。

多媒體範例是包含媒體資料之物件的參考。 若為影片影像，這是 DirectDraw 表面。 根據媒體類型 (音效、文字等等) ，範例的確切內容會有所不同。 因為範例只是資料物件的參考，所以任何數目的資料流程範例都可以參考相同的物件。 [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)介面會提供方法來取得和設定範例的特性，例如其開始和停止時間、狀態和資料流程關聯。 [**IStreamSample：： Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update)方法會在可讀取資料流程的情況下重新整理範例的資料。 針對可寫入資料流程，它會將範例的資料寫入至資料流程。 一般而言，您會在呈現、傳輸或儲存串流資料的迴圈中使用 **Update** 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於多媒體串流架構](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



