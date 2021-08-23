---
title: XML 標準化
description: XML 標準化可解決將一組 XML 節點轉換為位元組的問題，這種方式可讓 XML (的簡單變更，例如變更元素中屬性的順序) 不會變更產生的位元組格式。
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Windows 的 XML 標準化 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082982"
---
# <a name="xml-canonicalization"></a>XML 標準化

XML 標準化可解決將一組 XML 節點轉換為位元組的問題，這種方式可讓 XML (的簡單變更，例如變更元素中屬性的順序) 不會變更產生的位元組格式。 從標準化取得的位元組通常是用來透過 XML 內容產生密碼編譯簽章。


常用的 XML 標準化演算法可將下列層面標準化：

-   不含前序) 的字元編碼 (UTF-8
-   換行字元和其他字元形式
-   元素中的屬性順序
-   空白的元素表單
-   轉譯命名空間宣告

[**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)和 [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) api 會在讀取檔時提供 XML 標準化功能。

[**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)和 [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) api 會在寫入檔時提供 XML 標準化功能。

下列列舉適用于標準化：

-   [**WS \_ XML \_ 標準化 \_ 演算法**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**WS \_ XML \_ 標準化 \_ 屬性 \_ 識別碼**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

下列函式適用于標準化：

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

下列結構適用于標準化：

-   [**WS \_ XML \_ 標準化 \_ 內含 \_ 首碼**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**WS \_ XML \_ 標準化 \_ 屬性**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




