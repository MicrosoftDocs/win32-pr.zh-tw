---
description: WPD \_ 內容 \_ 類型 \_ 服務
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944899"
---
# <a name="wpd_content_type_service"></a>WPD \_ 內容 \_ 類型 \_ 服務

將其型別描述為 WPD \_ 內容 \_ 類型服務的物件 \_ 代表裝置服務。

這種類型的物件支援下列屬性。



| 屬性名稱                                                                                        | 必要或選擇性                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [WPD \_ 物件 \_ 識別碼](object-properties.md)                                               | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ 父 \_ 識別碼](object-properties.md)                                | 必要。                                                                      |
| [WPD \_ 物件 \_ 名稱](object-properties.md)                                           | 如果物件代表檔案，則為必要。                                      |
| [WPD \_ 物件 \_ 持續性 \_ 唯一 \_ 識別碼](object-properties.md)         | 必要、唯讀。 即使在建立時，用戶端也無法設定這個屬性。 |
| [WPD \_ 物件 \_ ISHIDDEN](object-properties.md)                                   | 如果不應該對使用者顯示服務，則為必要。                       |
| [WPD \_ 物件 \_ ISSYSTEM](object-properties.md)                                   | 如果物件為系統物件，則為必要項， (代表) 的系統檔案。          |
| [WPD \_ 功能 \_ 物件 \_ 類別](object-properties.md) | 必要。 這代表裝置服務類型。                             |
| [WPD \_ 服務 \_ 版本](object-properties.md)           | 必要。                                                                      |
| [WPD \_ 儲存體 \_ 類型](object-properties.md)                                                          | 如果服務用來儲存物件，則為必要項。                              |
| [WPD \_ 儲存體 \_ 容量](object-properties.md)                                                      | 如果服務用來儲存物件，則為必要項。                              |



 

## <a name="typical-resources"></a>一般資源

這些物件不會裝載資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 



