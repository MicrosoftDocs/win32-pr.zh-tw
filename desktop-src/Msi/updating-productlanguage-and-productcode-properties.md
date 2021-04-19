---
description: ProductLanguage 屬性必須更新為新語言 (LANGID) 的數值語言識別項。
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: 更新 ProductLanguage 和 ProductCode 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979389"
---
# <a name="updating-productlanguage-and-productcode-properties"></a>更新 ProductLanguage 和 ProductCode 屬性

[**ProductLanguage**](productlanguage.md)屬性必須更新為新語言 (LANGID) 的數值語言識別項。 在當地語系化範例的情況下， **ProductLanguage** 屬性的值必須從 LANGID for 英文 (1033) 變更為 [屬性資料表](property-table.md)中法文 (1036) 的 LANGID。

當地語系化資料庫時，[屬性資料表](property-table.md)中的 [ [**ProductCode**](productcode.md) ] 屬性值必須變更為新的唯一值，因為當地語系化的產品會視為不同的產品。 例如，應用程式的德文和英文版會視為兩個不同的產品，而且必須具有不同的產品代碼。 請參閱 [產品代碼](product-codes.md)。

您可以使用資料庫資料表編輯器來更新屬性工作表中的 [ProductCode] 和 [ProductLanguage] 屬性的值。 如果您複製此範例，請不要重複使用顯示的 GUID。

[屬性工作表](property-table.md)



| 屬性                                   | 值                                  |
|--------------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md)         | {EE389960-E426-4EEA-B669-AD8129249881} |
| [**ProductLanguage**](productlanguage.md) | 1036                                   |



 

[繼續](updating-a-summary-information-stream.md)

 

 



