---
description: 媒體基礎中的 ASF 支援
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: 媒體基礎中的 ASF 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db06c5a294e351b09d7f5327e8ee22891798671765bc5cc10eafd75785debde9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880953"
---
# <a name="asf-support-in-media-foundation"></a>媒體基礎中的 ASF 支援

媒體基礎支援 (ASF) 的 Advanced Systems 格式媒體檔案：

-   Windows媒體影片 (WMV 檔案) 
-   WindowsMedia Audio (WMA 檔案) 

媒體基礎提供數個物件來讀取和寫入 ASF 檔案。 這些物件是在兩個不同的架構層中提供。

首先， *管線* 層包含可在 [媒體基礎管線](media-foundation-pipeline.md) 內運作，且符合管線所定義之 api 的物件。 ASF 管線層包含：

-   [Asf 媒體來源](asf-media-source.md)：剖析 asf 檔案並傳遞音訊/影片資料封包。
-   [Windows 媒體編解碼器](windows-media-codecs.md)： Windows 媒體音訊或影片串流進行解碼或編碼。
-   [Asf 媒體接收器](asf-media-sinks.md)：接收資料封包並寫入 ASF 檔案。

其次，WM 容器層提供對剖析和寫入 ASF 檔案的低層級控制。 管線層會在內部使用 WMContainer。 應用程式也可以使用 WMContainer 進行低層級的 ASF 剖析和寫入。

![顯示管線層和 wm 容器元素的圖表](images/asf-components.png)

## <a name="in-this-section"></a>本節內容



| 主題                                                                         | 描述                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [ASF 檔案結構](asf-file-structure.md)<br/>                       | 介紹 ASF 檔案結構以及媒體基礎所提供的物件，以使用 ASF 檔案。<br/> |
| [管線層 ASF 元件](pipeline-layer-asf-components.md)<br/> | 說明如何使用管線層來剖析及撰寫 ASF 檔案。<br/>                                   |
| [WMContainer ASF 元件](wmcontainer-asf-components.md)<br/>       | 說明如何使用 WMContainer 層來剖析及撰寫 ASF 檔案。<br/>                                |



 

如需 ASF 檔案結構的詳細資訊，請參閱您可以從這個 [Microsoft 網站](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)下載的 asf 規格。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> </dl>

 

 




