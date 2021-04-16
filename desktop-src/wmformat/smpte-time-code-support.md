---
title: SMPTE 時間代碼支援
description: SMPTE 時間代碼支援
ms.assetid: 047bda0d-142d-4eed-9b59-c0c36b97ed45
keywords:
- Windows Media Format SDK、SMPTE 時間碼
- Advanced Systems Format (ASF) 、SMPTE 時間碼
- ASF (Advanced Systems Format) ，SMPTE 時間碼
- Windows Media Format SDK，IWMReaderTimecode 介面
- Advanced Systems Format (ASF) ，IWMReaderTimecode 介面
- ASF (Advanced Systems Format) ，IWMReaderTimecode 介面
- SMPTE 時間代碼，關於
- IWMReaderTimecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecf8ef9da7d0fb0ee7d973cf21129f307066bc9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104507796"
---
# <a name="smpte-time-code-support"></a>SMPTE 時間代碼支援

Windows Media Format SDK 提供有限的 SMPTE 時間代碼支援，這是適用于電影和電視的標準時間代碼格式。 您可以使用範例作為資料單位延伸模組來包含 SMPTE 時間代碼資料。 延伸模組的資料部分是 WMT 時間 [**\_ 碼 \_ 延伸模組 \_ 資料**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) 結構，其中包含來自原始 SMPTE 時間戳記的資訊。

在您的 ASF 檔案中維護 SMPTE 時間代碼會有效能限制。 具有相關聯之 SMPTE 時間戳記的每個範例，都需要在時間戳記結構中傳輸14個位元組。 在串流處理案例中，這種增加的頻寬需求可能會很嚴重。 因此，建議在影片編輯程式期間，僅將 SMPTE 時間代碼保存在 ASF 檔案中，這通常是使用本機檔案來完成。 建立最後的檔案時，您應該移除資料單位延伸模組。

您可以讀取「SMPTE 時間戳記」，就像讀取任何其他資料單位延伸一樣，但是讀取物件會提供以 SMPTE 時間碼搜尋的整合支援。 若要能夠搜尋 SMPTE 時間戳記，您必須先以 SMPTE 時間代碼為檔案編制索引。 您可以使用 [**IWMIndexer2：： configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure) 方法，將索引子設定為編制時間碼的索引。

使用非同步讀取器時，您可以使用 [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode) 介面的方法和 [**IWMReaderAdvanced3：： StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition) 方法，依 SMPTE 時間戳記流覽檔案。 使用同步讀取器時，請使用 [**IWMSyncReader2：： SetRangeByTimecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebytimecode)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**設定資料單位延伸模組**](configuring-data-unit-extensions.md)
</dt> </dl>

 

 




