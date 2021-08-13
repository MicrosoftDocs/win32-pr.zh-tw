---
description: 為新檔案撰寫 ASF 標頭物件
ms.assetid: f2a76471-3d93-427b-a316-d0967cd20e77
title: 為新檔案撰寫 ASF 標頭物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee50adc4e3f411bca9679672b88680ab3064bc91d828e2897ae1f94e40f9f9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355208"
---
# <a name="writing-an-asf-header-object-for-a-new-file"></a>為新檔案撰寫 ASF 標頭物件

ASF ContentInfo 物件會儲存檔案的 ASF 標頭物件資訊。 建立或修改 ASF 檔案時，必須產生標頭物件。 若要這樣做，應用程式必須將內容的編碼設定檔提供給 ContentInfo 物件，讓它知道要建立之媒體檔案的特性。

若要撰寫新的檔案，您可以使用 ContentInfo 物件來：

-   從要建立之檔案的設定檔物件收集標頭資訊。
-   在媒體基礎的內部維護 ASF 程式庫中的各種標頭物件。
-   初始化 asf 資料封包產生的 [asf](asf-multiplexer.md) 多工器，以及
-   以可寫入檔案的二進位格式來建立最上層的標頭物件。

如需設定檔的詳細資訊，請參閱 [ASF 設定檔](asf-profile.md)。

本節包含下列主題：



| 主題                                                                                                              | 描述                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [初始化新 ASF 檔案的 ContentInfo 物件](initializing-the-contentinfo-object-of-a-new-asf-file.md) | 描述 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 方法，該方法會使用儲存在設定檔物件中的標頭資訊來初始化 ContentInfo 物件。 |
| [在 ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)                   | 必須在 ContentInfo 物件上設定之各種設定屬性的相關資訊。                                                                                         |
| [產生新的 ASF 標頭物件](generating-a-new-asf-header-object.md)                                       | 如何從 ContentInfo 物件產生媒體緩衝區，其中包含新檔案的實際 ASF 標頭物件。                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF ContentInfo 物件](asf-contentinfo-object.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

ASF 檔案結構
</dt> </dl>

 

 



