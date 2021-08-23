---
title: 適用于 LDAP 提供者的 ADSI 物件模型
description: 此圖顯示用來存取這些物件的 LDAP 提供者和介面所使用的 ADSI 物件。
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c7c520793f6095bc9d4d9c6379f8ff6f09766f39ae6102f7e0a82d3a3de7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023788"
---
# <a name="adsi-object-model-for-ldap-providers"></a>適用于 LDAP 提供者的 ADSI 物件模型

下圖顯示用來存取這些物件的 LDAP 提供者和介面所使用的 ADSI 物件。

![ldap 提供者的物件模型](images/adsiobjmodldap-gif-1.png)

| Object                        | 介面                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 類別<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| 屬性<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [ **IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| GenObject<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)、 [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)、 [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)、 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)、 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)、 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| 命名空間<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)、 [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| RootDSE<br/>            | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| 路徑<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| 結構描述<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Syntax<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)、 [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| 組織<br/>       | [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| GroupCollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Group<br/>              | [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| UserCollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| 使用者<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| 位置<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)、 [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





