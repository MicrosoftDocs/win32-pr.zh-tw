---
title: 使用 IADs 介面
description: ADSI 中，目錄服務的每個專案都是以 ADSI 物件來表示，它是一種元件物件模型， (COM) 物件，此物件支援標準 COM IUnknown 介面以及 IDispatch 和 IADs 介面。
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- 使用 IADs ADSI
- ADSI ADSI，使用 IADs 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878afa9350a45f18238bebb69df1a96eba52715e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382873"
---
# <a name="using-the-iads-interfaces"></a>使用 IADs 介面

ADSI 中，目錄服務的每個專案都是以 ADSI 物件來表示，它是一種元件物件模型， (COM) 物件，此物件支援標準 COM [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面以及 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 和 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面。 **IADs** 提供 ADSI 物件的基本維護功能。

每個 ADSI 物件都必須支援這個介面，此介面可用於：

-   依名稱、類別或 ADsPath 提供物件識別。
-   識別管理建立和刪除物件的物件容器。
-   取得物件架構定義。
-   將物件屬性載入至屬性快取，並將變更認可至持續性目錄存放區。
-   存取和修改屬性快取中的物件屬性值。

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面的設計目的，是要確保 ADSI 物件能以有效率且一致的方式來呈現各種基礎目錄服務，以提供網路系統管理員和目錄服務提供者。

![支援 iads 介面的 adsi 物件](images/ds2iads.png)

上圖顯示一般的 ADSI 物件，它支援基本介面 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)、 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)。 這類 ADSI 物件可透過支援的介面，管理來自基礎目錄服務之資料存放區的資料。 這項資料稱為物件的屬性，而取得和設定這些屬性的常式則稱為屬性方法。 唯讀屬性有一個可取得屬性值的屬性方法。 讀取/寫入屬性有兩種方法：設定值的方法，以及可取得值的方法。 屬性會在每個使用 [屬性](the-adsi-attribute-cache.md)快取的 ADSI 物件上執行。 [**IADs：： get \_ADsPath**](iads-property-methods.md) 和 **IADs：:p 的 ui \_ ADsPath** 是屬性方法的範例。 屬性方法對 Visual Basic 以及啟用屬性之直接參考的其他 Automation 用戶端來說並不明顯。 例如，Visual Basic 使用 **物件. adspath** 語法直接參考 **IADs：： adspath** 。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

此外，ADSI 物件也會與其他 ADSI 物件互動，並透過方法直接與命名空間進行互動。 方法會立即執行。 方法的範例包括 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 和 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)。

屬性（property）、屬性（property）方法和方法都可透過標準 COM 介面存取。

ADSI 物件是由其 ADsPath 唯一識別。 例如，LDAP 命名空間的 ADsPath 是 "LDAP://MyServer/DC=Fabrikam,DC=COM"。 如需 ADsPaths 的詳細資訊，請參閱 [ADSI](binding-to-an-adsi-object.md)系結。 針對熟悉 COM 名字標記的程式設計人員，這在概念上類似于 COM 的標記顯示名稱。

包含其他 ADSI 物件的 ADSI 物件（稱為 ADSI 容器物件）也支援 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面，這個介面會提供方法和屬性，以管理物件所包含的 ADSI 物件的建立、刪除和列舉。 下圖顯示 ADSI 容器物件。

![adsi 容器物件](images/dsiadsc.png)

大部分的 ADSI 物件都是由其他物件所包含。 唯一沒有父容器的 ADSI 物件是最上層的 ADSI **命名空間** 物件 ( 「ADS：」 ) 。

容器物件的 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法會持續將 ADSI 容器物件的快取屬性儲存至儲存體，以及使用 [**IADsContainer：： Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) 方法建立的任何物件。 [**IADsContainer：:D elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) 不會影響屬性快取，但會刪除這個物件所代表的基礎命名空間目錄元素。

 

 