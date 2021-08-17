---
description: 產品代碼是 GUID，也就是應用程式或產品的主體識別。
ms.assetid: 6fbad59b-27b7-4ac1-bad5-8a608c7b270f
title: 產品代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2afe0c96e78d14bc989d4acdc7195d374b82466c4b345a999df7085468587e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145371"
---
# <a name="product-codes"></a>產品代碼

產品代碼是 GUID，也就是應用程式或產品的主體識別。 如需詳細資訊，請參閱 [ [**ProductCode**](productcode.md) ] 屬性。 如果對產品進行重大變更，則產品代碼也應該變更以反映這一點。 但是，如果產品的變更相對較小，則不需要變更產品程式碼。

應用程式套件的32位和64位版本必須有不同的產品代碼。 如果應用程式的任何32位元件重新編譯成64位元件，則必須指派新的產品代碼。

如果 [PublishComponent 資料表](publishcomponent-table.md) 中公開的伺服器是從32位重新編譯為64位，則可能也需要變更此資料表中的 GUID，讓32位和64位用戶端可以識別適當的限定元件類別。 在此情況下，產品代碼也必須變更。

請注意，產品程式碼 Guid 中的字母必須為大寫。 GUIDGEN 之類的公用程式會產生包含小寫字母的 Guid。 這些 Guid 中的小寫字母必須變更為大寫，才能當做產品代碼或封裝程式碼使用。 如需詳細資訊，請參閱 [變更產品代碼](changing-the-product-code.md)。

封裝程式碼是識別特定 Windows Installer [*套件*](p-gly.md)的 GUID。 封裝程式碼會將 .msi 檔案與應用程式或產品產生關聯，也可以用於驗證來源。 產品和套件代碼不可互換。 沒有兩個 nonidentical .msi 檔應該要有相同的套件程式碼。 雖然傳送具有相同封裝程式碼和產品程式碼的應用程式很常見，但在更新應用程式時，這兩個值可能會分離出來。 如需詳細資訊，請參閱 [封裝程式碼](package-codes.md)。

 

 



