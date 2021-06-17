---
title: " (Windows Media Format 11 SDK) 的屬性"
description: 深入瞭解 Windows Media Format 11 SDK 中的屬性。 屬性是中繼資料的個別專案。
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262190"
---
# <a name="attributes-windows-media-format-11-sdk"></a> (Windows Media Format 11 SDK) 的屬性

屬性是中繼資料的個別專案。 大部分的屬性都可以由您的應用程式設定，並寫入至 ASF 檔案的標頭。

某些預先定義的屬性是編碼屬性。 這些屬性不會儲存在 ASF 檔案的標頭中，而是在載入檔案時由 Windows Media Format SDK 的物件所計算。 因為程式碼屬性一律會進行計算，所以它們本質上是唯讀的。

此 SDK 包含許多您可以使用的屬性定義。 您也可以建立自己的屬性來描述內容。

下列各節說明預先定義的屬性。



| 區段                                                                | 描述                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [屬性清單](attribute-list.md)                                   | 提供所有預先定義之屬性的字母順序清單。 在清單之後，每個屬性都會個別描述。                                                                          |
| [具有多個值的屬性](attributes-with-multiple-values.md) | 列出可以新增至檔案一次以上的屬性。                                                                                                                                      |
| [依類型的屬性](attributes-by-type.md)                           | 包含依類型排序的屬性清單。 這些屬性包括特殊用途的屬性清單 (例如處理數位版權管理) 的屬性，以及依內容類型的建議屬性清單。 |
| [ID3 標記支援](id3-tag-support.md)                                 | 列出與 ID3 標記相容的屬性。                                                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**使用中繼資料**](working-with-metadata.md)
</dt> </dl>

 

 




