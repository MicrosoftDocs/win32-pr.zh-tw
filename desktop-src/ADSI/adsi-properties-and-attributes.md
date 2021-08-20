---
title: ADSI 屬性和屬性
description: 屬性（attribute）有時也稱為屬性（property）。 這可能會造成混淆。 本檔會使用下列屬性和屬性定義。
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Adsi 屬性和屬性 ADSI
- ADSI ADSI、使用、存取及運算元據、屬性和屬性
- ADSI 屬性
- 屬性 ADSI
- 屬性 ADSI，已定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082792"
---
# <a name="adsi-properties-and-attributes"></a>ADSI 屬性和屬性

屬性（attribute）有時也稱為屬性（property）。 這可能會造成混淆。 本檔會使用下列屬性和屬性定義。

屬性是與程式設計物件相關聯的名稱值。 例如， [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面會公開屬性，例如 [**類別**](iads-property-methods.md) 和 **名稱**。

屬性是與目錄服務中的物件相關聯的資料。 例如，使用者物件將會有一個名為 **cn** 的屬性，其中包含的字串是物件的一般或相對分辨名稱。 您可以透過 ADSI 介面方法（例如 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 和 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put)）來存取屬性。

如需 ADSI 屬性和屬性的詳細資訊，請參閱：

-   [ADSI 屬性快取](the-adsi-attribute-cache.md)
-   [Single 與 Multiple Value 屬性](single-vs--multiple-value-attributes.md)
-   [Active Directory 操作屬性](active-directory-operational-attributes.md)

 

 




