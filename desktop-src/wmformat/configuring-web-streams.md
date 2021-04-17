---
title: 設定 Web 資料流程
description: 設定 Web 資料流程
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- 資料流程，設定 Web 資料流程
- 編解碼器，設定 Web 串流
- Web 串流，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301851"
---
# <a name="configuring-web-streams"></a>設定 Web 資料流程

Web 串流是一種特殊類型的檔案傳輸資料流程，用來在單一資料流程中傳遞與網站相關聯的檔案。 下表摘要說明 Web 串流設定。



| 設定                                            | Description                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| **WM \_ 媒體 \_ 類型。 majortype**                      | 設定為 WMMEDIATYPE \_ FileTransfer。                                                 |
| **WM \_ 媒體 \_ 類型。子類型**                        | 設定為 WMMEDIASUBTYPE \_ WebStream。                                                 |
| **WM \_ 媒體 \_ 類型。 bFixedSizeSamples**              | 設定為 False。                                                                     |
| **WM \_ 媒體 \_ 類型。 bTemporalCompression**           | 設定為 [True]。                                                                      |
| **WM \_ 媒體 \_ 類型。 lSampleSize**                    | 設定為0。                                                                         |
| **WM \_ 媒體 \_ 類型。 formattype**                     | 設定為 WMFORMAT \_ WebStream。                                                       |
| **WM \_ 媒體 \_ 類型。 pUnk**                           | 設定為 **Null**。                                                                  |
| **WM \_ 媒體 \_ 類型。 cbFormat**                       | 設定為 `sizeof(WMT_WEBSTREAM_FORMAT)`。                                            |
| **WM \_ 媒體 \_ 類型。 pbFormat**                       | 設定為正確設定的 **WMT \_ WEBSTREAM \_ 格式** 結構位址。 |
| **WMT \_ WEBSTREAM \_ FORMAT. cbSampleHeaderFixedData** | 設定為 `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`。                                     |
| **WMT \_ WEBSTREAM \_ FORMAT. wVersion**                | 設定為 1。                                                                         |
| **WMT \_ WEBSTREAM \_ FORMAT. wreserved**               | 設定為0。                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Web 串流**](web-streams.md)
</dt> </dl>

 

 




