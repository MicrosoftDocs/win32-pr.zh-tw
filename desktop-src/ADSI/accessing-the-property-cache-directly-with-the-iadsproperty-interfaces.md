---
title: 存取具有 IADsProperty 介面的屬性快取
description: IADsProperty 介面包含 IADsPropertyList、IADsPropertyEntry 和 IADsPropertyValue。
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- 使用 IADsProperty 介面 ADSI 直接存取屬性快取
- 屬性快取 ADSI
- 屬性快取 ADSI，使用 IADsProperty 介面存取屬性快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/04/2019
ms.locfileid: "103932843"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>存取具有 IADsProperty 介面的屬性快取

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)介面包含 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)、 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)。 這些介面會提供方法來直接存取和操作物件快取的屬性。 屬性（property）稱為屬性專案（property），並對應至架構中定義的屬性（property）。 屬性專案可以有一個或多個屬性值。 一組屬性專案會組織為屬性清單。

[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)介面會管理 ADSI 物件的屬性清單。 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)介面會為屬性專案執行這項作業。 同樣地， [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) 介面代表一個或多個屬性值。 它們一起提供一種機制，讓使用者能夠：

-   直接使用屬性快取。
-   使用不含架構的目錄，例如 LDAP 版本2伺服器。

[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* 介面會嚴格地在屬性快取上運作，而且不會嘗試與伺服器互動，以取得或修改持續性存放區中的資料。 因此，這些介面只能用來檢查及操作用戶端快取中的屬性。 在使用這些介面之前，您必須明確地呼叫 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法或 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 方法，以將物件屬性載入至快取中（如果快取尚未初始化）。 呼叫這些介面的方法之後，您必須呼叫 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 來保存基礎目錄存放區的變更。

如需可用來執行這些介面的詳細資訊和程式碼範例，請參閱 [使用 IADsProperty 介面存取屬性快取的範例程式碼](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)。

 

 




