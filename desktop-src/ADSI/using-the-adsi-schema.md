---
title: 使用 ADSI 架構
description: 架構會定義儲存在目錄中的物件 universe。
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 架構
- Adsi ADSI，使用 ADSI 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaf49f75d026f52c644d06a6fe36e4555841e3e7bf587ffeb1e0277d1e5ac99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648818"
---
# <a name="using-the-adsi-schema"></a>使用 ADSI 架構

架構會定義儲存在目錄中的物件 universe。 在 Active Directory 中，架構會指定目錄服務物件可以或必須擁有的屬性。 它也會指定屬性的值範圍和語法，以及它們是否支援單一或多個值。 簡單地說，架構是依類別定義、屬性定義和屬性語法來組織。 ADSI 提供三個介面，可讓您從架構讀取屬性、類別和語法資料： [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)和 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)。

Active Directory 會使用一組架構物件來提供可動態擴充的架構管理。 如需未知物件的詳細資訊，請查閱其相關聯的架構物件。 若要建立新的類別定義或擴充現有的類別定義，您可以建立或擴充適當的架構物件。 架構物件會組織在指定目錄的架構容器中。 若要存取物件架構類別，請使用物件的 [**IADs**](iads-property-methods.md) 屬性來取得 ADsPath 字串，然後使用該字串來系結至物件架構類別上的 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面。

若要判斷屬性定義（也就是值的範圍、語法等等），請檢查目錄服務物件所支援之每個屬性的架構屬性物件。 如需有關如何存取架構屬性物件的詳細資訊，請參閱 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)。

ADSI 會視需要將語法資料抽象化，並可讓您使用 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) 來識別表示物件資料所需的語法。

如需 Active Directory 架構的詳細資訊，請參閱 [Active Directory 架構](/windows/desktop/AD/active-directory-schema)。 如需用來讀取架構容器的程式碼範例，請參閱 [讀取架構](reading-the-schema.md)。

 

 