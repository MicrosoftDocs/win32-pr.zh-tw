---
description: 關於轉碼 API
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: 關於轉碼 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449770"
---
# <a name="about-the-transcode-api"></a>關於轉碼 API

下圖顯示轉碼 API 與媒體基礎編碼管線的其餘部分之間的關聯。

![顯示轉碼 api 的圖表。](images/encoding08.png)

編碼管線包含下列資料處理物件：

-   媒體來源
-   解碼器
-   影片尺寸調整或音訊 resampler
-   編碼器
-   媒體接收器

只有當輸出影片的大小與來源不同時，才需要影片尺寸調整器。 只有當音訊需要在編碼之前重新取樣時，才需要音訊 resampler。 必須要有解碼/編碼器組，才能進行轉碼，但無法用於 remuxing。

編碼 *拓撲* 是一組管線物件， (來源、解碼器、調整器、resampler、編碼器和媒體接收器) ，以及兩者之間的連接點。 如需拓撲的詳細資訊，請參閱 [拓撲](topologies.md)。

不同的元件會負責建立各種管線物件：

-   應用程式通常會使用 [來源解析程式](source-resolver.md) 來建立媒體來源。
-   [媒體會話](media-session.md)會載入並設定「解碼器」、「影片調整」和「音訊 resampler。 就內部而言，它會使用拓撲載入器來進行這 (請參閱 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)) 。
-   轉碼 API 會載入並設定編碼器和媒體接收器。

Advanced applications 可以直接設定編碼器和媒體接收，而不是使用轉碼 API。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉碼 API](transcode-api.md)
</dt> <dt>

[使用轉碼 API](fast-transcode-objects.md)
</dt> </dl>

 

 



