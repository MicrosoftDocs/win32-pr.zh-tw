---
description: 可以在文字欄位中使用可設定資料的索引鍵格式類型，在資料庫資料表中提供索引鍵。
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: 索引鍵格式類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970615"
---
# <a name="key-format-types"></a>索引鍵格式類型

可以在文字欄位中使用可設定資料的索引鍵格式類型，在資料庫資料表中提供索引鍵。 MsmConfigItemNonNullable 屬性是此資料格式的隱含，不需要設定。 Null 對此類型而言永遠不是有效的值。 所有索引鍵格式專案的回應都必須採用 [CMSM 的特殊格式](cmsm-special-format.md)。

存在下列索引鍵格式類型：

[目錄類型](directory-type.md)

[檔案類型](file-type.md)

[屬性類型](property-type.md)

[對話方塊類型](dialog-type.md)

[二進位類型](binary-type.md)

[圖示類型](icon-type.md)

索引鍵格式類型的可設定專案會在文字資料行中用來提供資料庫索引鍵，而且一般可以由任何文字字串取代。 個別類型可能會有其他語法限制，但是 Mergemod.dll 不會強制執行這些限制。 特定可設定的專案也可能具有特性語義限制。 例如，可能需要特定的可設定專案成為 [二進位資料表](binary-table.md) 中包含點陣圖影像的資料列的索引鍵。 Mergemod.dll 不會強制執行這類限制，因此模組作者應該準備好處理任何符合指定之索引鍵格式類型的字串。 除非以語義意義或屬性另有指定，否則 null 是有效的回應。

 

 



