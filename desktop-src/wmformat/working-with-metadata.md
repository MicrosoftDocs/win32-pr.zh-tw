---
title: 使用中繼資料
description: 使用中繼資料
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK，中繼資料總覽
- Advanced Systems Format (ASF) ，中繼資料總覽
- ASF (Advanced Systems Format) ，中繼資料總覽
- 中繼資料，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104374817"
---
# <a name="working-with-metadata"></a>使用中繼資料

中繼資料支援是由寫入器物件、讀取器和同步讀取器物件，以及中繼資料編輯器物件提供。 如需中繼資料的一般資訊，請參閱 [中繼資料](metadata.md)。 如需有關在 Windows Media 格式 SDK 中支援中繼資料之功能的詳細資訊，請參閱 [中繼資料功能](metadata-features.md)。

中繼資料編輯的介面是 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)，您可以藉由呼叫上述其中一個物件中任何介面的 **QueryInterface** 方法來取得該介面。 **IWMHeaderInfo3** 會繼承 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 和 [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)的方法。 處理中繼資料屬性的 **IWMHeaderInfo3** 方法代表存取中繼資料的不同方法，而不是 **IWMHeaderInfo** 方法所使用的方法。 您應該一律使用較新的方法。

ASF 檔案中的中繼資料是由索引和資料流程號碼來識別。 檔案層級屬性會指派為0的資料流程編號。 在舊版的 Windows Media Format SDK 中，可以依名稱來識別屬性。 不過，因為您現在可以在資料流程中複製屬性名稱，所以無法再使用。 相反地，您可以取出所有符合名稱的索引。 如需詳細資訊，請參閱 [取出中繼資料屬性](retrieving-metadata-attributes.md)。

為了協助快速尋找屬性，您可以使用特殊的串流號碼0xFFFF。 您可以使用此資料流程號碼來識別整個檔案，而不是特定的資料流程或檔案層級的屬性。 Windows Media Format SDK 的物件會針對每個資料流程和檔案層級屬性維護不同的索引。 使用 stream 0xFFFF 時，索引與您指定特定資料流程時所用的索引不同。 例如，資料流程0的索引0屬性不會與 stream 0xFFFF 的索引0屬性相同。

下列各節會更詳細地說明中繼資料的使用方式。



| 區段                                                                    | 描述                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [正在抓取中繼資料屬性](retrieving-metadata-attributes.md)       | 說明如何從檔案標頭讀取中繼資料屬性。                     |
| [設定中繼資料屬性](setting-metadata-attributes.md)             | 說明如何將新的中繼資料屬性加入至檔案標頭。                    |
| [編輯中繼資料屬性](editing-metadata-attributes.md)             | 描述如何編輯現有的中繼資料屬性。                               |
| [移除中繼資料屬性](removing-metadata-attributes.md)           | 描述如何移除現有的中繼資料屬性。                             |
| [使用複雜的中繼資料屬性](using-complex-metadata-attributes.md) | 描述如何使用其值以結構表示的屬性。 |



 

數個範例應用程式會示範如何取出和編輯中繼資料。 尤其是，請參閱 MetadataEdit 範例，這會同時隨附于 c + + 和 c # 版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> <dt>

[**範例應用程式**](sample-applications.md)
</dt> </dl>

 

 




