---
title: 建立和刪除物件
description: 使用 ADSI 時，會使用 IADsContainer 或 IDirectoryObject 介面來建立和刪除物件。
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- 建立和刪除物件 ADSI
- ADSI、建立及刪除物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4730c4cc6a95ad37bfd3953474d3d488fcf05abb
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463704"
---
# <a name="creating-and-deleting-objects"></a>建立和刪除物件

使用 ADSI 時，會使用 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 或 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面來建立和刪除物件。

## <a name="creating-an-object-with-iadscontainer"></a>使用 IADsContainer 建立物件

**使用 IADsContainer 介面建立物件**

1.  系結至將包含要建立之物件的容器，並取得 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) 建立方法，在容器中建立新的物件。
3.  使用 [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 或 [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法，為物件設定所有必要屬性的值。 建立物件所需的屬性將取決於目錄服務和建立的物件類型。 如需建立 Active Directory 物件的詳細資訊，請參閱 [建立和刪除 Active Directory 物件](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)。
4.  使用 [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 或 [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) 方法，為物件設定所有所需的選擇性屬性值。
5.  呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法來認可物件和其屬性。 在呼叫 **IADs. SetInfo** 方法來認可屬性之前，不會實際在基礎目錄服務中建立新的物件。

## <a name="creating-an-object-with-idirectoryobject"></a>使用 IDirectoryObject 建立物件

**使用 IDirectoryObject 介面建立物件**

1.  系結至將包含要建立之物件的容器，並取得 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面。
2.  配置 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 結構的陣列，其中包含建立物件時要設定之每個屬性的一個結構。
3.  針對物件的每個必要屬性填入 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 結構。 建立物件所需的屬性將取決於目錄服務和建立的物件類型。 如需建立 Active Directory 物件的詳細資訊，請參閱 [建立和刪除 Active Directory 物件](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)。
4.  針對物件的每個選擇性屬性，填入 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 結構。
5.  使用 [**IDirectoryObject：： CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) 方法，在容器中建立物件。 這個方法也會將物件認可至基礎目錄服務。 如果 [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 陣列未包含物件的所有必要屬性， **IDirectoryObject：： CreateDSObject** 將會失敗。

## <a name="deleting-an-object"></a>刪除物件

若要刪除物件，請使用 [**IADsContainer：:D elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) 或 [**IDirectoryObject：:D eletedsobject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) 方法。 如果已刪除的物件包含任何子物件，這些方法將會失敗。 使用 [**IADsDeleteOps：:D eleteobject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) 方法來刪除容器以及容器的所有子物件。

刪除的物件會發生什麼事取決於基礎目錄服務。 如需刪除 Active Directory 物件的詳細資訊，請參閱 [建立和刪除 Active Directory 物件](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services)。

 

 