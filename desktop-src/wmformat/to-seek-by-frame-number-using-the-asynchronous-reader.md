---
title: 使用非同步讀取器依框架編號搜尋
description: 使用非同步讀取器依框架編號搜尋
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF) ，依框架編號搜尋
- ASF (Advanced Systems Format) ，依框架編號搜尋
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，依框架編號搜尋
- 影片串流，依畫面格編號搜尋
- 影片串流，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e218384b1a27bb3240ac74ad9af6d8298945bb57dfaf635531cb4cbb9aaa9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432611"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>使用非同步讀取器依框架編號搜尋

您可以使用非同步讀取器物件，在 ASF 檔案中搜尋影片資料流程的框架數。 若要使用以框架為基礎的搜尋，讀取器中載入的檔案必須依框架編制索引。 每個個別的影片串流都可以建立索引。 若要判斷資料流程是否已依框架編制索引，您可以 \_ 呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)來檢查檔案標頭中的 g wszWMNumberOfFrames 屬性。

若要使用非同步讀取器依框架號碼在 ASF 檔案中搜尋資料，請執行下列步驟。

1.  藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)介面的指標。
2.  藉由呼叫 [**IWMReaderAdvanced3：： StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)來設定開始畫面格編號和持續時間。 您必須指定框架索引影片資料流程的串流號碼。 讀取器會將輸出的其餘部分與指定之資料流程的指定框架的呈現時間進行同步處理，並開始傳遞輸出範例。
3.  如同您在 **IWMReaderCallback：： OnSample** 方法的實中一般地處理範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**在播放時讀取中繼資料**](reading-metadata-at-playback.md)
</dt> <dt>

[**使用索引**](working-with-indexes.md)
</dt> </dl>

 

 




