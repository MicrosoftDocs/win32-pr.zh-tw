---
title: 擴充架構
description: Active Directory Directory 服務架構會定義 Active Directory Domain Services 中所使用的屬性和類別。
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory，使用架構，擴充架構
- 架構 AD，擴充架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189556"
---
# <a name="extending-the-schema"></a>擴充架構

Active Directory Directory 服務架構會定義 Active Directory Domain Services 中所使用的屬性和類別。 包含在系統中的基底架構包含一組豐富的類別定義，例如 **使用者**、 **電腦** 和 **organizationalUnit**，以及屬性定義，例如 **userPrincipalName**、 **telephoneNumber** 和 **objectSid**。 現有的類別和屬性集合對大部分的應用程式都已足夠。 不過，架構是可擴充的，這表示您可以定義新的類別和屬性。 本節討論如何延伸 Active Directory 架構。

## <a name="when-to-extend-the-schema"></a>延伸架構的時機

如果現有的類別和屬性不符合您想要儲存的資料類型，您應該擴充架構。 請務必注意，架構新增是永久性的;您可以停用類別和屬性，但是絕對不能從架構中移除它們。 當您測試程式碼時，請記住這一點。

也請考慮您要儲存的資料大小。 Microsoft 建議沒有任何屬性值超過 500 kb，包括多值屬性的總和。 此外，物件的大小不能超過 1 mb。 也請考慮資料的實例數目;如果您在具有100000使用者的系統上，將新屬性新增至 [**使用者**](/windows/desktop/ADSchema/c-user) 類別，這可能會佔用相當大的空間。

本節中的主題包括：

-   如何系結至架構容器，以及讀取現有類別和屬性的屬性。
-   如何及何時透過定義新的屬性和類別來延伸架構。
-   如何使用 LDIFDE、CSVDE 或以程式設計方式使用 ADSI 安裝架構延伸。

如需 Active Directory 架構的詳細資訊和總覽，包括架構執行、類別定義和屬性定義的相關資訊，請參閱 [Active Directory 架構](active-directory-schema.md)。

如需詳細資訊，包括預先定義之架構類別、屬性和屬性語法的參考頁面，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)中的 Active Directory 架構參考。

 

 