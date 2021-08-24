---
description: 為了避免不同物件所建立的屬性發生名稱衝突，共用屬性管理員 (SPM) 使用共用屬性群組。
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: 共用屬性群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cda375c09b164e4ed380ba7d89477f2225b5b6004f98299ec9fd9b46f80abee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029211"
---
# <a name="shared-property-groups"></a>共用屬性群組

為了避免不同物件所建立的屬性發生名稱衝突，共用屬性管理員 (SPM) 使用共用屬性群組。 共用屬性群組只是一組共用屬性的命名空間。 共用屬性群組中的每個屬性都包含名稱、值和共用屬性群組內的位置。 您可以使用名稱或位置來取得屬性值。 您可以透過共用屬性群組管理員來存取和建立共用屬性群組。

下圖顯示 SPM 物件模型。

![顯示 SPM 物件模型的圖表： ISharedPropertyGroupManager、ISharedPropertyGroup 到 ISharedProperty。](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

以下是共用屬性管理員的介面：

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) 可用來建立共用屬性群組，以及取得現有共用屬性群組的存取權。 您可以使用 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)或 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)來建立 [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)物件的實例，以存取 **ISharedPropertyGroupManager** 介面。

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) 是用來建立及存取共用屬性群組中的共用屬性。 您可以使用 [**ISharedPropertyGroupManager：： CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup)方法來建立 [**SharedPropertyGroup**](sharedpropertygroup.md)物件，以存取 **ISharedPropertyGroup** 介面。 如同任何 COM 物件一樣，您必須在使用完 **SharedPropertyGroup** 物件之後，再加以釋放。

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) 可用來設定或抓取共用屬性的值。 共用屬性可包含任何可由 Variant 表示的資料類型。 您可以使用 [**ISharedPropertyGroup：： CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)方法或 [**ISharedPropertyGroup：： CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立 [**SharedProperty**](sharedproperty.md)物件，以存取 **ISharedProperty** 介面。 只能從 [**SharedPropertyGroup**](sharedpropertygroup.md)物件內建立或存取 **SharedProperty** 物件。 同樣地，當您使用完 **SharedProperty** 物件時，必須釋放它。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 共用屬性管理員](com--shared-property-manager.md)
</dt> </dl>

 

 
