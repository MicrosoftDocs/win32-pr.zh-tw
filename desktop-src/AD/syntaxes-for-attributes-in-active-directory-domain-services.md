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
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092618"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a><span data-ttu-id="355e8-105">Active Directory Domain Services 中的屬性語法</span><span class="sxs-lookup"><span data-stu-id="355e8-105">Syntaxes for Attributes in Active Directory Domain Services</span></span>

<span data-ttu-id="355e8-106">Active Directory Domain Services 定義一組屬性語法，以指定屬性所包含的資料類型。</span><span class="sxs-lookup"><span data-stu-id="355e8-106">Active Directory Domain Services define a set of attribute syntaxes for specifying the type of data contained by an attribute.</span></span> <span data-ttu-id="355e8-107">預先定義的語法實際上並不會出現在目錄中，而且您無法加入新的語法。</span><span class="sxs-lookup"><span data-stu-id="355e8-107">The predefined syntaxes do not actually appear in the directory, and you cannot add new syntaxes.</span></span> <span data-ttu-id="355e8-108">您可以使用數種方法來識別屬性類別的語法：</span><span class="sxs-lookup"><span data-stu-id="355e8-108">Several methods can be used to identify the syntax of an attribute class:</span></span>

-   <span data-ttu-id="355e8-109">[**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get)、 [**IADs. GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex)、 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put)、 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-putex)方法會使用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)結構來取得和設定物件屬性的值。</span><span class="sxs-lookup"><span data-stu-id="355e8-109">The [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs.GetEx**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs.Put**](/windows/desktop/api/iads/nf-iads-iads-put), and [**IADs.PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) methods use the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure to get and set the values of an object's attributes.</span></span> <span data-ttu-id="355e8-110">這個結構的 **vt** 成員是識別資料型別的 **VARTYPE** 值。</span><span class="sxs-lookup"><span data-stu-id="355e8-110">The **vt** member of this structure is a **VARTYPE** value that identifies the data type.</span></span>
-   <span data-ttu-id="355e8-111">[**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject)和 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)介面的方法會使用 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)列舉中的值來指定資料類型。</span><span class="sxs-lookup"><span data-stu-id="355e8-111">The methods of the [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) interfaces use a value from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration to specify the data type.</span></span>
-   <span data-ttu-id="355e8-112">若要指定新屬性類別的語法，請設定 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax)和 [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax)屬性。</span><span class="sxs-lookup"><span data-stu-id="355e8-112">To specify the syntax of a new attribute class, set the [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) and [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) attributes of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object.</span></span> <span data-ttu-id="355e8-113">如果 **oMSyntax** 的值是127，您也必須設定 [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) 屬性。</span><span class="sxs-lookup"><span data-stu-id="355e8-113">If the value of **oMSyntax** is 127, you must also set the [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) attribute.</span></span> <span data-ttu-id="355e8-114">如需詳細資訊，請參閱 [選擇語法](choosing-a-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="355e8-114">For more information, see [Choosing a Syntax](choosing-a-syntax.md).</span></span>

<span data-ttu-id="355e8-115">如需 Active Directory Domain Services 所提供語法的完整清單，包括每個語法的對應 **VARTYPE** 和 [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) 值，請參閱 [語法](/windows/desktop/ADSchema/syntaxes)。</span><span class="sxs-lookup"><span data-stu-id="355e8-115">For a complete list of the syntaxes provided by Active Directory Domain Services, including each syntax's corresponding **VARTYPE** and [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value, see [Syntaxes](/windows/desktop/ADSchema/syntaxes).</span></span>

 

 