---
title: 關於轉換流程
description: 關於轉換流程
ms.assetid: 147b82fd-9e82-4acf-8f8a-43eb02e99024
keywords:
- Windows Media Player，轉換流程
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6fe2f2bbedf03b78c0d19abaf3793e8e92c788
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023059"
---
# <a name="about-the-conversion-process"></a>關於轉換流程

在 Windows Media Player 具現化轉換外掛程式之後，程式會繼續進行，如下所示：

1.  播放機會呼叫 [IWMPConvert：： ConvertFile](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpconvert-convertfile)。
2.  外掛程式會將 *bstrInputFile* 參數中提供的檔案轉換成 ASF 格式。
3.  如果轉換因某些原因而失敗，外掛程式會傳回適當的失敗代碼，並停止處理常式。
4.  如果轉換成功，外掛程式會將轉換後的檔案放入 *bstrDestinationFolder* 參數中提供的資料夾，並透過 *pbstrOutputFile* 參數傳回已轉換之檔案的完整路徑。
5.  外掛程式會從 **ConvertFile** 傳回成功碼。
6.  播放程式會將轉換過的檔案複製到使用者的 [音樂] 資料夾階層中的資料夾。 播放玩家複製檔案的確切位置，取決於內容。 在這個過程中，播放程式可能會重新命名檔案。
7.  播放程式會將原始 (未轉換的) 檔案複製到使用者的 [音樂] 資料夾階層中的資料夾。 在這個過程中，播放程式可能會重新命名檔案。 這是使用者將內容從電腦同步處理到需要源檔案格式的裝置時，播放程式所使用的檔案複本。 這個檔案稱為「陰影檔案」（ *shadow file*）。
8.  播放機會將已轉換之檔案的相關資訊新增至文件庫。 這包括將 **ShadowFilePath** 屬性的值設定為儲存陰影檔的新位置。

如果您需要使用已轉換的檔案，您可以使用 **ContentDistributor** 和 **WM/UniqueFileIdentifier** 屬性，查詢程式庫以取得內容。 如果您需要使用陰影檔案，您仍然必須取出已轉換之檔案的 **媒體** 物件，然後查詢 **ShadowFilePath** 屬性。 請參閱 [將中繼資料新增至轉換](adding-metadata-to-converted-files.md)的檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於轉換外掛程式**](about-conversion-plug-ins.md)
</dt> <dt>

[**將中繼資料新增至轉換的檔案**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**讀取屬性值**](reading-attribute-values.md)
</dt> <dt>

[**ShadowFilePath 屬性**](shadowfilepath-attribute.md)
</dt> <dt>

[**WM/ContentDistributor 屬性**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**WM/UniqueFileIdentifier 屬性**](wm-uniquefileidentifier-attribute.md)
</dt> </dl>

 

 




