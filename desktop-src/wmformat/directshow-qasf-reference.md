---
title: DirectShowQASF 參考
description: DirectShowQASF 參考
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows媒體格式 SDK，QASF
- Windows媒體格式 SDK，DirectShow
- DirectShow，QASF 參考
- QASF 篩選準則，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69029c02945f181ba8faa631c3320f461ddbf650ed337cdf895ee5204a57de21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655659"
---
# <a name="directshow-qasf-reference"></a>DirectShowQASF 參考

本章節包含下列 DirectShow QASF 篩選器、介面和列舉的程式設計參考。 DirectShow SDK 檔包含這些篩選器所公開的其他泛型介面（例如 **IBaseFilter** 和 **IPin**），以及舊版 QASF 元件的參考和程式設計指南。

如需 QASF 名稱的說明，請參閱[關於 DirectShow](about-directshow.md)。

下列篩選準則包含在 DirectShow QASF 元件中。



| 篩選                                           | Description                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [WM ASF 讀取器篩選器](wm-asf-reader-filter.md) | 讀取及剖析本機或遠端 ASF 檔案。                      |
| [WM ASF 寫入器篩選器](wm-asf-writer-filter.md) | 從壓縮或未壓縮的輸入資料流程建立 ASF 檔案。 |



 

下列介面是為了與 DirectShow QASF 元件搭配使用而定義的。



| 介面                                                  | 描述                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | 提供一種方法，可讓應用程式從 [WM Asf 寫入](wm-asf-writer-filter.md) 器的輸入 Pin 或 [wm asf 讀取](wm-asf-reader-filter.md) 器篩選器的輸出圖釘註冊回呼。 用於索引編制和新增資料單位延伸模組時。 |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | 由應用程式執行，並由篩選準則呼叫。 應用程式會在此介面上使用一個方法，以取得資料流程中個別範例的相關資訊。 用於索引編制和新增資料單位延伸模組時。                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | 在 WM ASF 寫入器上執行。 由應用程式用來指定檔案的設定檔和索引參數。                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | 在 WM ASF 寫入器上提供額外的設定函數。                                                                                                                                                                                                             |



 

已定義下列列舉、結構和事件，以搭配 DirectShow QASF 元件使用。



| 列舉型別                                                               | 描述                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | 定義 [**IConfigAsfWriter2：： GetParam**](iconfigasfwriter2-getparam.md) 和 [**SetParam**](iconfigasfwriter2-setparam.md) 方法中所使用的篩選設定參數。 |



 



| 結構                                         | 描述                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WMT \_ 事件 \_ 資料**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | 包含與 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)事件有關的資訊，以及 Windows 媒體格式 SDK 所傳回之相關聯的狀態碼。 |



 



| 事件                                           | 描述                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [EC \_ WMT \_ 活動](ec-wmt-event.md)              | 從 Windows 媒體格式 SDK 轉送的事件。                                                              |
| [EC \_ WMT \_ 索引 \_ 事件](ec-wmt-index-event.md) | 當應用程式使用[WM ASF 寫入器](wm-asf-writer-filter.md)來編制 Windows Media 視訊檔案的索引時傳送。 |



 

 

 