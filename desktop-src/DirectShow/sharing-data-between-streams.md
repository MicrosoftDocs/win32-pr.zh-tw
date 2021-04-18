---
description: 在資料流程之間共用資料
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: 在資料流程之間共用資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467755"
---
# <a name="sharing-data-between-streams"></a>在資料流程之間共用資料

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

處理多媒體資料通常需要大量的系統資源;因此，您應該盡可能避免複製資料。 串流架構支援共用的資料流程範例，這是一種機制，可將資料從某個資料流程移至另一個資料流程，而不需要複製它。 即使目的地資料流程未特別支援基礎資料格式，這個緩衝區仍能在兩個數據流之間有效率地傳輸資料。

例如，假設您有一個具有三個數據流的多媒體資料流程：影片和音訊，以及 URL 資料的時間戳記，以符合影片內容。 您想要撰寫一個應用程式，以在每個影片畫面上新增著作權注意事項，並將資料寫入另一個串流以進行儲存，但您的應用程式不了解影片串流以外的任何資料格式。 針對影片串流，您可以建立附加至所需 DirectDraw 表面的範例。 然後，您可以呼叫 [**IDirectDrawMediaStream：： CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) 方法，並將該指標指向相同的介面，或 [**IMediaStream：： CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample)，以建立輸出資料流程。 在這兩種情況下，輸入和輸出資料流程都會共用 DirectDraw 表面。 因為您瞭解影片格式，所以您可以視需要存取這個介面。

若要抓取其他來來源資料流指標 (音訊和 URL) ，請列舉來源容器資料流程並抓取 nonvideo 資料流程的指標。 每個來來源資料流在輸出資料流程容器中都有相關聯的輸出資料流程。 藉由呼叫輸出容器上的 [**IMultiMediaStream：： GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) 方法和每個來來源資料流指標，來取出這些輸出指標。 下列步驟說明這個程序。

1.  呼叫 [**IMultiMediaStream：： EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) 來取得來來源資料流的指標。 請確定它不是影片串流，因為您的應用程式已經瞭解其格式。
2.  使用步驟1中的指標，在輸出容器資料流程上呼叫 [**IMultiMediaStream：： GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) 。 這會傳回所要輸出資料流程的指標。
3.  在來來源資料流上呼叫 [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) 。
4.  在輸出資料流程上呼叫 [**CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) 。
5.  呼叫來來源資料流上的 [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ，以讀取資料。
6.  呼叫輸出資料流程上的 [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) 來寫入資料。

針對您不支援其格式的每個資料流程重複這些步驟。 當兩個範例都完成更新時，輸出資料流程會有來自來來源資料流的所有資料，而且您已完成。

 

 



