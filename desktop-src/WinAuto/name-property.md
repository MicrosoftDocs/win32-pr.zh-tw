---
title: Name 屬性
description: Name 屬性是用戶端用來為使用者識別、尋找或宣告物件的字串。 所有物件都支援 Name 屬性。
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996556"
---
# <a name="name-property"></a>Name 屬性

**Name** 屬性是用戶端用來為使用者識別、尋找或宣告物件的字串。 所有物件都支援 **Name** 屬性。

例如，按鈕控制項上的文字是其名稱，而清單方塊或編輯控制項的名稱則是在控制項的定位順序中緊接在控制項前面的靜態文字。 即使是未顯示名稱的繪圖物件，在查詢 **name** 屬性時也會提供文字。

藉由呼叫 [**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)，即可取出 **Name** 屬性。

## <a name="selecting-names"></a>選取名稱

物件的名稱應該是直覺的，讓使用者瞭解物件的意義或用途。 此外，[ **名稱** ] 屬性應該是唯一的，相對於父系中的任何同級物件。

資料表內的導覽會對某些使用者造成特別困難的問題。 因此，伺服器開發人員應該盡可能使資料表單元格名稱成為描述性。 例如，您可以藉由結合所佔用的資料列和資料行的名稱（例如 "A1"）來建立資料格名稱。 不過，通常最好使用更具描述性的名稱，例如 "南，二月"，其中 "南" 是目前的資料列，而 "二月" 是目前的資料行。

## <a name="delegating-requests"></a>委派要求

如果物件沒有其 **Name** 屬性的存取權，它就會將要求委派給其父系，並依其子識別碼進行識別。 例如，如果用戶端呼叫編輯控制項的 [ **名稱** ] 屬性，則編輯控制項會將查詢委派給其父系，以傳回標記編輯控制項的靜態文字控制項值。

 

 




