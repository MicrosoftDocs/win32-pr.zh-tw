---
title: 將屬性包含在通用類別目錄中
description: 樹系的通用類別目錄包含樹系中每個物件的部分複本。
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- 包含在通用類別目錄 AD 中的屬性
- 包含在通用類別目錄中的屬性 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462937"
---
# <a name="including-attributes-in-the-global-catalog"></a>將屬性包含在通用類別目錄中

樹系的通用類別目錄包含樹系中每個物件的部分複本。 針對每個物件，通用類別目錄只會包含每個物件屬性的子集。 如果屬性已複寫至通用類別目錄， [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)屬性會設定為 **TRUE** 。

具有下列特性的屬性適用于通用類別目錄中的儲存體：

-   屬性是全域有趣的，因為找出可能發生在樹系中任何位置的物件，或因為無法存取完整的物件，而對屬性的讀取存取是很重要的。 第一個型別的範例是 [**location**](/windows/desktop/ADSchema/a-location) 屬性，它可以用來尋找 [**列印佇列**](/windows/desktop/ADSchema/c-printqueue) 物件。 第二種類型的範例是 [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)，因為即使您無法存取其 [**使用者**](/windows/desktop/ADSchema/c-user) 物件的完整複本，也可以呼叫某人。
-   屬性的變動性很低。 這點很重要，因為如果屬性類別包含在通用類別目錄中，則整個企業樹系中該屬性類別之每個值的變更都會複寫至企業中的所有通用類別目錄伺服器。
-   屬性值的大小很小。 "Small" 具有高度主觀：將屬性放在通用類別目錄中，請考慮將屬性複寫至企業中所有通用類別目錄伺服器的影響。 屬性越小，影響愈低。 因為只有在屬性變更時才會發生複寫，所以複寫的影響也會隨著變動性的減少而變小，因此具有極低變動性的大型屬性可能會有較大的整體影響，而不是具有高變動性的小型屬性。

決定是否要將屬性放在通用類別目錄中時，請記住，您在通用類別目錄伺服器上的交易增加複寫和增加磁片儲存空間，可能會加快查詢效能。 一般而言，您會使用通用類別目錄來搜尋感興趣的物件，以便您可以讀取物件的選取屬性。 如果您感興趣的屬性已複寫至通用類別目錄，則可以直接從通用類別目錄讀取它們。 或者，若要讀取未複寫至通用類別目錄的屬性，您必須執行其他步驟來取得它們。 在此情況下，在搜尋通用類別目錄以尋找感興趣的物件之後，您必須從通用類別目錄讀取物件的辨別名稱，使用 DN 直接系結至物件的完整複本（可能位於不同的伺服器上），最後從物件的完整複本讀取非通用類別目錄屬性。

經常查詢及參考的屬性（例如員工名稱和電話號碼）很適合包含在通用類別目錄中。 不常參考的屬性（例如 "driverVersion"），最好是從通用類別目錄中排除。

 

 