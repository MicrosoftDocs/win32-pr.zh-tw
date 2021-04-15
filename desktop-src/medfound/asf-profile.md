---
description: 本主題說明如何在 Microsoft 媒體基礎中使用 ASF 設定檔。
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: ASF 設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510826"
---
# <a name="asf-profile"></a>ASF 設定檔

本主題說明如何在 Microsoft 媒體基礎中使用 ASF 設定檔。

Advanced Systems Format (ASF) 檔案包含一或多個資料流程。 針對每個資料流程，ASF 標頭包含描述資料流程的資料流程屬性標頭。 在 [WMContainer](wmcontainer-asf-components.md) 層，下列物件會用來設定或讀取 ASF 資料流程的屬性：

-   *ASF 設定檔* 物件：描述資料流程及其與彼此之間的關聯性。 ASF 設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。
-   *串流* 設定物件：描述一個資料流程。 資料流程設定物件包含描述資料流程格式的媒體類型。 針對音訊和影片串流，媒體類型會確切描述資料流程的設定方式，並由編解碼器編碼或解碼資料流程使用。 Stream configuration 物件會公開 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面。 有效的 ASF 設定檔至少包含一個資料流程設定物件。
-   *相互排除* 物件：描述不會同時讀取的多個資料流程。 相互排除物件會公開 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) 介面。 ASF 設定檔包含零或多個相互排除物件。

下圖顯示 ASF 設定檔與設定檔中所包含之物件之間的關聯性。

![具有串流設定子節點之 asf 設定檔節點的樹狀結構圖;第一個指向媒體類型，接下來的兩個對相互排除](images/asf-components02.png)

為了播放，會使用 ASF 設定檔來列舉資料流程並尋找資料流程格式。 若為編碼，則會使用 ASF 設定檔來設定目的地檔案中的資料流程。

ASF 設定檔也用來設定 [Asf 媒體接收器](asf-media-sinks.md)。 針對 ASF 設定檔中的每個資料流程，ASF 媒體接收器會建立對應的資料流程接收。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                           | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [建立 ASF 設定檔](creating-an-asf-profile.md)<br/>                               | 說明如何建立 ASF 設定檔物件。<br/>          |
| [建立和設定 ASF 資料流程](creating-and-configuring-asf-streams.md)<br/>     | 說明如何將資料流程新增至 ASF 設定檔。<br/>         |
| [針對 ASF 資料流程使用相互排除](using-mutual-exclusion-for-asf-streams.md)<br/> | 說明如何將相互排除專案新增至 ASF 資料流程。 <br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[教學課程： 1-傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[教學課程：使用 CBR 編碼方式撰寫 WMA 檔案](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> </dl>

 

 




