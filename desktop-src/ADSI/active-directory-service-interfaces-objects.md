---
title: Active Directory 服務介面物件
description: ADSI 物件模型包含 COM 物件。 用戶端會使用介面來操作物件。 ADSI 提供者會執行物件和其介面。
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- 物件 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842723"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory 服務介面物件

ADSI 物件模型包含 COM 物件。 用戶端會使用介面來操作物件。 ADSI 提供者會執行物件和其介面。

ADSI 物件是代表目錄服務中專案的 COM 物件：電腦、使用者、檔案、伺服器、印表機、列印佇列等等。也就是網路系統管理員每天都能使用的元素。 ADSI 定義不同類型的物件來表示不同種類的元素。 如下圖所示，每個物件都支援一個或多個可存取物件資料（通常稱為中繼資料）的 COM 介面。

![active directory 服務介面物件](images/ds2objex.png)

因為 COM 介面是以邏輯方式連接的屬性和方法集合，所以您可以將每個介面視為物件的控制碼，以便一次只提供一組邏輯函式的存取權。 下表列出基本的 ADSI 元素。



| 介面            | 描述                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | 用於物件識別。 作為所有 ADSI 物件所需的基本介面， [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 會提供物件中繼資料的存取權，包括其在 ADSI 架構中的定義。 IADs 也會提供屬性和方法的存取權，這些屬性和方法會管理屬性快取中的物件資料。                                                                                   |
| **IADsContainer**    | 用於物件管理和偵測。 所有 ADSI 容器物件都需要 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面來管理物件的建立、刪除、複製和移動、系結和列舉。                                                                                                                                                                      |
| **IADsPropertyList** | 用於物件屬性管理。 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)介面會優化屬性快取中物件資料的管理。                                                                                                                                                                                                                                |
| **IDirectoryObject** | 用於直接物件存取。 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面可針對未使用自動化的用戶端提供低層級的物件存取。 這個介面會略過物件屬性快取，並提供物件屬性的直接存取。 如需詳細資訊，請參閱 [IADs 和 IDirectoryObject 介面](the-iads-and-idirectoryobject-interfaces.md)。 |
| **IUnknown**         | 用於 COM 物件管理。 所有 COM 物件都需要 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面。                                                                                                                                                                                                                                                                              |
| **IDispatch**        | 用於型別程式庫資料和方法調用。 所有 Automation 物件都需要 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面。                                                                                                                                                                                                                             |



 

更複雜的 ADSI 物件可能會公開額外的介面。 例如， [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) 支援管理相同資料類型之目錄元素集合的方法。 [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) 方法會管理支援 [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) 介面之物件的特殊大小寫集合。 針對支援的提供者， [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面支援查詢目錄服務的方法。 此外，ADSI 提供的介面代表知名的邏輯和實體專案。 例如，代表使用者的 ADSI 物件支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)，代表電腦的支援 [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)等等。 如需 ADSI 物件的詳細資訊，請參閱 [IADs 和 IDirectoryObject 介面](the-iads-and-idirectoryobject-interfaces.md)。 並非所有提供者都會在所有介面上執行所有介面或所有方法和屬性。 如需詳細資訊，請參閱 [ADSI 參考](adsi-reference.md)。

 

 