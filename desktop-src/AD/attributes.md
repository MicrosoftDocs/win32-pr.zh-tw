---
title: '屬性 (AD DS) '
description: Active Directory Domain Services 中的每個物件都包含一組屬性，這些屬性會定義物件的特性。
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- 屬性廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023290"
---
# <a name="attributes-ad-ds"></a>屬性 (AD DS) 

Active Directory Domain Services 中的每個物件都包含一組屬性，這些屬性會定義物件的特性。 定義屬性的架構容器中的 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件會描述每個屬性。 屬性定義包含各種資料，例如，屬性適用的物件類型，以及屬性的語法類型。 如需屬性架構定義的詳細資訊，請參閱 [屬性的](characteristics-of-attributes.md)特性。

下列清單列出 Active Directory Domain Services 中儲存的屬性類型。

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>已複寫網域的儲存屬性
</dt> <dd>

某些屬性會儲存在目錄 (例如 [**cn**](/windows/desktop/ADSchema/a-cn)、 [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)和 [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) ，並複寫到網域中的所有網域控制站。 這些屬性的子集也會複寫到通用類別目錄。 如果您從通用類別目錄列舉物件的屬性，則只會傳回復寫至通用類別目錄的屬性。 某些屬性也會編制索引，因為在查詢中包含索引屬性可改善查詢效能。

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>非複寫的本機儲存屬性
</dt> <dd>

非複寫的屬性（例如 [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)、 [**上次登入**](/windows/desktop/ADSchema/a-lastlogon)和 [**上次登出**](/windows/desktop/ADSchema/a-lastlogoff) ）會儲存在每個網域控制站上，但不會複寫。 非複寫的屬性是與特定網域控制站相關的屬性。 例如，[ **上次登入** ] 屬性是使用者的網路登入由傳回屬性的特定網域控制站進行驗證的最後一個日期和時間。 您可以用與先前所述網域範圍屬性相同的方式來抓取這些屬性。 不過，針對這些屬性，每個網域控制站只會儲存與該特定網域控制站相關的值。 例如，若要取得使用者上次登入網域的時間，請從網域中的每個網域控制站取出使用者的 **最後一個登入** 屬性，並尋找最新的日期和時間。

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>非儲存的結構化屬性
</dt> <dd>

使用者物件也具有未儲存在目錄中的已建立屬性，但是是由網域控制站（例如 [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) 和 [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes)）所計算。

</dd> </dl>

 

 