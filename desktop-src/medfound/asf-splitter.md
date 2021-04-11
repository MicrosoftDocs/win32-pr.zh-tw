---
description: ASF 分隔器
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: ASF 分隔器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111888"
---
# <a name="asf-splitter"></a>ASF 分隔器

ASF *分隔器* 物件是 WMContainer 層元件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。 您可以使用分隔器來讀取資料物件中的資料封包，並產生資料流程範例。 如需 ASF 檔案結構的詳細資訊，請參閱 [asf 檔案結構](asf-file-structure.md)。

分隔器會公開 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面。 分割器會針對選取的資料流程剖析 ASF 資料封包，並將其重新封裝為公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的個別範例物件。 分隔器是媒體基礎的平台層級元件之一。 ASF 媒體來源會在內部使用分隔器來剖析 ASF 檔。

下圖說明如何透過分隔器產生 ASF 檔案的範例。

![顯示 asf 檔案產生範例的圖表](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

本節包含下列主題：



| 主題                                                                                                                        | 描述                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [建立 ASF 分隔器物件](creating-the-asf-splitter-object.md)                                                     | 如何建立及初始化分隔器。                              |
| [設定 ASF 分隔器物件](configuring-the-asf-splitter-object.md)                                               | 分隔器的設定。                                |
| [從現有的 ASF 資料物件產生資料流程範例](generating-stream-samples-from-an-existing-asf-data-object.md) | 如何剖析 ASF 資料物件並產生 packetized 流範例。 |



 

下表顯示相關的資料物件屬性。



| 屬性                                                                                                    | 描述                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**](mf-pd-asf-fileproperties-packets-attribute.md)                   | ASF 資料物件中的資料封包數目。                                                       |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最小封 \_ 包 \_ 大小**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | 檔案中的資料封包大小下限（以位元組為單位）。                                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 封 \_ 包 \_ 大小上限**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | 檔案中資料封包的大小上限（以位元組為單位）                                               |
| [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md)                                         | ASF 資料物件的大小（以位元組為單位）。                                                               |
| [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md)                            | 相對於檔案開頭之 ASF 資料物件中第一個資料封包的位移（以位元組為單位）。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> <dt>

[教學課程：讀取 ASF 檔案](tutorial--reading-an-asf-file.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



