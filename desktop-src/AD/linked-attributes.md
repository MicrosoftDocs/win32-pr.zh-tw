---
title: '連結屬性 (AD DS) '
description: 連結的屬性是一組屬性，其中系統會根據另一個屬性上設定的值，在整個樹系中 (轉寄連結) ，來計算一個屬性的值 () 後置連結。
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- 連結的屬性廣告
- 屬性 AD、連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2167169d6a9d2f8eabe69323054767ae66823d8e1fe954a232ed63fd31a9b845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186991"
---
# <a name="linked-attributes-ad-ds"></a>連結屬性 (AD DS) 

連結的屬性是一組屬性，其中系統會根據另一個屬性上設定的值，在整個樹系中 (轉寄連結) ，來計算一個屬性的值 () 後置連結。 任何物件實例上的後置連結值，都是由在對應的轉寄連結中設定物件之 DN 的所有物件的 DNs 所組成。 例如，「管理員」和「報表」是一組連結的屬性，其中經理是轉寄連結，而報表是「上一頁」連結。 現在假設帳單是 Joe 的經理。 如果您將帳單的使用者物件的 DN 儲存在 Joe 的 user 物件的 "Manager" 屬性中，則 Joe 的 user 物件的 DN 會顯示在帳單的使用者物件的 "Reports" 屬性中。

向前連結/後置連結配對是由兩個 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)定義的 [**linkID**](/windows/desktop/ADSchema/a-linkid)值所識別。 轉寄連結的 **linkID** 是偶數、非零的值，而相關聯的上一頁連結的 **linkID** 則是轉寄 **linkID** 加1。 例如，"Manager" 的 **linkID** 是42，而 "Reports" 的 **linkID** 是43。

以下是定義一組新連結屬性的指導方針清單：

-   [**LinkID**](/windows/desktop/ADSchema/a-linkid)值在所有 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件中都必須是唯一的。 若要避免衝突，您應該依照 [取得連結識別碼](obtaining-a-link-id.md)主題中的指示，自動產生 **linkID** 。
-   [上一頁] 連結必須有對應的 [轉寄] 連結，也就是在建立對應的 [後置連結] 屬性之前，向前連結必須存在。
-   後置連結一律是多值屬性。 轉寄連結可以是單一值或多重值。 如果有多對多關聯性，請使用多重值的向前連結。
-   轉寄連結的 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 值必須是2.5.5.1、2.5.5.7 或2.5.5.14。 這些值會對應至包含辨別名稱的語法，例如 [**(DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) 語法的物件。
-   後置連結的 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 值必須是2.5.5.1，也就是 [**(DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) 語法的物件。
-   依照慣例，會將後置連結屬性新增至 [**最上層**](/windows/desktop/ADSchema/c-top)抽象類別的 [**mayContain**](/windows/desktop/ADSchema/a-maycontain)值。 這可讓您從任何類別的物件讀取後置連結屬性，因為它們不會實際與物件一起儲存，而是根據轉寄連結值來計算。

 

 