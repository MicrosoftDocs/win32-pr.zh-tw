---
title: 中繼資料編輯器物件
description: 中繼資料編輯器物件
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows媒體格式 SDK，中繼資料編輯器物件
- Advanced Systems Format (ASF) 的中繼資料編輯器物件
- ASF (Advanced 系統格式) ，中繼資料編輯器物件
- 物件，中繼資料編輯器物件
- 中繼資料編輯器物件，關於
- 中繼資料、編輯器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8e78aaf6ada96a9cefa1a9ec6f4aa5708c7382539bc3b75493734c18d600b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027446"
---
# <a name="metadata-editor-object"></a>中繼資料編輯器物件

中繼資料編輯器物件是用來編輯儲存在 ASF 檔案標頭區段中的資訊。 此物件最常操作的專案是中繼資料屬性。 此外，中繼資料編輯器會處理 [*標記*](wmformat-glossary.md) 和指令碼命令。 只有當您想要編輯現有檔案的標頭而不播放時，才需要使用 [中繼資料編輯器]。

中繼資料編輯器物件是由函式 [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)所建立，它會將指標設定為 **IWMMetadataEditor** 介面。 您可以藉由呼叫 **QueryInterface** 方法，取得中繼資料編輯器物件的其他介面。

中繼資料編輯器物件支援下列介面。



| 介面                                        | 描述                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | 可讓編輯應用程式檢查 ASF 檔案的 [*DRM*](wmformat-glossary.md) 屬性，而不需要任何許可權來播放受保護的內容。 |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | 操縱標頭中的屬性、標記和指令碼命令。                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | 抓取編解碼器資訊。 繼承 **IWMHeaderInfo** 的所有方法。                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | 提供屬性的先進支援，包括大型屬性、多語言和重複的屬性名稱。 繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | 開啟、關閉，並將變更儲存至 ASF 檔案的標頭。                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | 使用多個檔案存取和共用選項開啟 ASF 檔案以進行標頭編輯。 繼承 **IWMMetadataEditor** 的所有方法。                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**標記**](markers.md)
</dt> <dt>

[**中繼資料**](metadata.md)
</dt> <dt>

[**物件**](objects.md)
</dt> <dt>

[**指令碼命令**](script-commands.md)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




