---
title: Active Directory 服務介面架構
description: 許多目錄服務都是階層式的，因此會成為階層式物件模型。 本節使用 COM 物件表示來說明各種 ADSI 功能。
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory 服務介面架構 ADSI
- ADSI ADSI，關於，架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671196"
---
# <a name="active-directory-service-interfaces-architecture"></a>Active Directory 服務介面架構

許多目錄服務都是階層式的，因此會成為階層式物件模型。 本節使用 COM 物件表示來說明各種 ADSI 功能。

在下列物件模型圖中，最上層系統物件會針對每個已安裝的 ADSI 提供者，各包含一個命名空間物件。

![命名空間容器物件](images/ds2top.png)

每個命名空間物件本身都是一個容器，其中包含每個伺服器、網域的最上層根節點，或任何其他類型的目錄系統物件在每個目錄服務中定義為根目錄。

ADSI 提供一組預先定義的物件和介面，讓用戶端應用程式可以使用一組統一的方法與目錄服務互動。 不過，ADSI 可能無法提供目錄服務的所有功能存取權。 為了更妥善地使用每個目錄服務的完整功能集，ADSI 提供了一種架構模型，可讓目錄服務提供者和協力廠商軟體廠商用來擴充 ADSI 中所提供之介面以外的功能。

根節點容器物件（位於每個提供者命名空間物件內）包含 ADSI 架構容器物件。 此物件包含該提供者之所有功能的定義。 如需詳細資訊，請參閱 [ADSI 架構模型](adsi-schema-model.md)。

本節包含下列主題：

-   [Active Directory 服務介面物件](active-directory-service-interfaces-objects.md)
-   [命名空間](namespaces.md)
-   [Active Directory 服務介面提供者](active-directory-service-interfaces-provider.md)
-   [ADSI 架構模型](adsi-schema-model.md)

 

 




