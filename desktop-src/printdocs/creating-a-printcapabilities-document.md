---
description: 當 PrintTicket 經過驗證之後，就可以用來建立 PrintCapabilities 的快照集。
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: 建立 PrintCapabilities 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a01395df674b683349bd4a5f42fe1bd57ef2768ef4d967ba3aeda7734f5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950198"
---
# <a name="creating-a-printcapabilities-document"></a>建立 PrintCapabilities 檔

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

當 PrintTicket 經過驗證之後，就可以用來建立 PrintCapabilities 的快照集。 提供者必須有任何屬性的內部標記法，其值相依于裝置設定。 例如，如果 SpotDiameter 是一種相依于解析和媒體類型功能的屬性，則 SpotDiameter 的內部標記法會與不同的解析和媒體值相關聯，如下表所示：



| 解決方法      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | 債券<br/>   | 520<br/> |
| 300<br/>  | 光澤<br/> | 350<br/> |
| 600<br/>  | 債券<br/>   | 330<br/> |
| 600<br/>  | 光澤<br/> | 180<br/> |
| 1200<br/> | 債券<br/>   | 250<br/> |
| 1200<br/> | 光澤<br/> | 100<br/> |



 

在此範例中，PrintCapabilities 提供者必須使用提供的 PrintTicket，從內部資料表和報表中選取適當的專案，做為 SpotDiameter 屬性的值。 對於值相依于設定) 的每個屬性，每個多重值屬性 (都會重複此程式。 [PrintCapabilities 架構和檔結構](printcapabilities-schema-and-document-construction.md)一節說明建立 PrintCapabilities 快照集時所牽涉到的其他步驟。

若要建立預設 PrintCapabilities 檔的快照集，請提供預設的 PrintTicket (，而不是建立 PrintCapabilities 檔之方法的任意 PrintTicket) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




