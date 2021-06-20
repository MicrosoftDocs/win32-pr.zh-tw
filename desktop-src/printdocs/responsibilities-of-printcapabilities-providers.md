---
description: PrintCapabilities 提供者必須支援 PrintTicket/PrintCapabilities 提供者介面所隱含的最小一組功能。
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: PrintCapabilities 提供者的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404911"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>PrintCapabilities 提供者的責任

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

PrintCapabilities 提供者必須支援 PrintTicket/PrintCapabilities 提供者介面所隱含的最小一組功能。 這裡列出這些功能。

-   它們必須遵循傳播的方向嗎？XML 屬性（當它出現在適當的內容中，並且包含該內容的有效值時）。

-   它們必須產生符合 PrintCapabilities 架構的 PrintCapabilities 檔，並滿足列印架構中所指定的需求。

-   他們必須能夠辨識有效的 PrintTicket。

-   他們必須能夠解讀 PrintTicket，並瞭解它所代表的特定設定。

-   他們必須能夠判斷該設定是否包含條件約束衝突。

-   它們必須能夠修改無效或衝突的 PrintTicket，方法是進行必要的最少重大變更，使其有效且不會發生衝突。

-   他們必須能夠產生特定裝置設定的 PrintCapabilities 檔。

-   他們必須能夠產生預設設定或 PrintTicket。

-   他們必須能夠產生對應至預設設定的 PrintCapabilities 檔。

-   他們必須實行設備磁碟機所定義的選項評分程式，能夠判斷屬於相同功能的兩個選項實例之間的相符接近程度。 此演算法用於 PrintTicket 驗證程式。

除了上述需求以外，PrintCapabilities 檔必須針對每個 XML 屬性包含有效且正確的值 (例如，每個選項的限制) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



