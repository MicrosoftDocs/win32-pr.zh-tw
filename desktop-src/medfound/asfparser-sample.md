---
description: ASFParser 範例
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: ASFParser 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db441be45d28899bc8f2ace68b8f09af40e679449d26aec7adf25ab4fb9e2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959548"
---
# <a name="asfparser-sample"></a>ASFParser 範例

說明如何使用媒體基礎中的低層級 ASF 元件，從 Advanced 系統格式剖析資料 (ASF) 檔。 此範例會示範下列工作：

-   列舉 ASF 檔案中的音訊和影片串流。
-   選取音訊或影片串流進行剖析。
-   在所需的播放時間搜尋封包。
-   正在為選取的資料流程產生壓縮的範例。
-   解碼音訊和影片範例。

## <a name="apis-demonstrated"></a>示範的 Api

這個範例會示範下列 Microsoft 媒體基礎介面：

-   [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a>使用方式

1.  若要開啟 ASF 檔案，請按一下 [ **開啟媒體** 檔案] 按鈕。
2.  選取 ASF 檔案，然後按一下 [ **開啟**]。 檔案的相關資訊會顯示在 **資訊** 窗格中。
3.  在 [剖析器設定 **] 下，** 選取要剖析的資料流程。
4.  若要反向產生樣本，請選取 [ **反向**]。
5.  若要指定起始點，請將滑杆拖曳至所要的位置。
6.  若要開始剖析，請按一下 [ **產生範例** ] 按鈕。 範例的相關資訊會顯示在 **資訊** 窗格中。
7.  若要測試音訊串流的範例，請按一下 [ **測試音訊** ] 按鈕。
8.  若要測試影片串流的範例，請按一下 [ **顯示點陣圖** ] 按鈕。

## <a name="requirements"></a>規格需求



| 產品                                                        | 版本   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>下載範例

此範例可在[Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)中取得。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎 SDK 範例](media-foundation-sdk-samples.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> <dt>

[教學課程：讀取 ASF 檔案](tutorial--reading-an-asf-file.md)
</dt> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> </dl>

 

 



