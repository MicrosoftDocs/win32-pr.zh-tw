---
title: DirectShow QASF 參考
description: DirectShow QASF 參考
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK、QASF
- Windows Media Format SDK、DirectShow
- DirectShow、QASF 參考
- QASF 篩選準則，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375953"
---
# <a name="directshow-qasf-reference"></a>DirectShow QASF 參考

本章節包含下列 DirectShow QASF 篩選器、介面和列舉的程式設計參考。 DirectShow SDK 檔包含這些篩選器所公開的其他泛型介面（例如 **IBaseFilter** 和 **IPin**），以及舊版 QASF 元件的參考和程式設計指南材質。

如需 QASF 名稱的說明，請參閱 [關於 DirectShow](about-directshow.md)。

DirectShow QASF 元件包含下列篩選。



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



 

已定義下列列舉、結構和事件以搭配 DirectShow QASF 元件使用。



| 列舉型別                                                               | 描述                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | 定義 [**IConfigAsfWriter2：： GetParam**](iconfigasfwriter2-getparam.md) 和 [**SetParam**](iconfigasfwriter2-setparam.md) 方法中所使用的篩選設定參數。 |



 



| 結構                                         | Description                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WMT \_ 事件 \_ 資料**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | 包含與 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 事件有關的資訊，以及 WINDOWS Media 格式 SDK 所傳回的相關狀態碼。 |



 



| 事件                                           | 描述                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [EC \_ WMT \_ 活動](ec-wmt-event.md)              | 從 Windows Media 格式 SDK 轉送的事件。                                                              |
| [EC \_ WMT \_ 索引 \_ 事件](ec-wmt-index-event.md) | 當應用程式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來編制 Windows Media 視訊檔案的索引時傳送。 |



 

 

 