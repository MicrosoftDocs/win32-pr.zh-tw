---
title: 適用于 LDAP 提供者的 ADSI 物件模型
description: 此圖顯示用來存取這些物件的 LDAP 提供者和介面所使用的 ADSI 物件。
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ee06c6bbcfc96a84cc3e7f679d7a13988a78b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931863"
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
| User<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| 位置<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)、 [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





