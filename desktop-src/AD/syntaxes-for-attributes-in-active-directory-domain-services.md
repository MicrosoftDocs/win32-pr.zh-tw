---
title: Active Directory Domain Services 中的屬性語法
description: Active Directory Domain Services 定義一組屬性語法，以指定屬性所包含的資料類型。
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services 屬性的語法 Active Directory
- 屬性 Active Directory，語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c324fef5267ce37b42ede66b618b33148d266ac52dd69662a15bbce6094951ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182836"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Active Directory Domain Services 中的屬性語法

Active Directory Domain Services 定義一組屬性語法，以指定屬性所包含的資料類型。 預先定義的語法實際上並不會出現在目錄中，而且您無法加入新的語法。 您可以使用數種方法來識別屬性類別的語法：

-   [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get)、 [**IADs. GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex)、 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put)、 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-putex)方法會使用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構來取得和設定物件屬性的值。 這個結構的 **vt** 成員是識別資料型別的 **VARTYPE** 值。
-   [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)和 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)介面的方法會使用 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)列舉中的值來指定資料類型。
-   若要指定新屬性類別的語法，請設定 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax)和 [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax)屬性。 如果 **oMSyntax** 的值是127，您也必須設定 [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) 屬性。 如需詳細資訊，請參閱 [選擇語法](choosing-a-syntax.md)。

如需 Active Directory Domain Services 所提供語法的完整清單，包括每個語法的對應 **VARTYPE** 和 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 值，請參閱 [語法](/windows/desktop/ADSchema/syntaxes)。

 

 