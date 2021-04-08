---
title: 關於 Active Directory 架構
description: Active Directory Domain Services 中的每個物件都是 Active Directory 架構中所定義之物件類別的實例。
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839091"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="d2553-103">關於 Active Directory 架構</span><span class="sxs-lookup"><span data-stu-id="d2553-103">About the Active Directory Schema</span></span>

<span data-ttu-id="d2553-104">Active Directory Domain Services 中的每個物件都是 Active Directory 架構中所定義之物件類別的實例。</span><span class="sxs-lookup"><span data-stu-id="d2553-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="d2553-105">物件類別代表物件目錄，例如使用者、印表機或應用程式，它們都共用一組共同特性。</span><span class="sxs-lookup"><span data-stu-id="d2553-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="d2553-106">每一個物件類別的定義都包含可用來說明類別之執行個體的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="d2553-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="d2553-107">例如，使用者類別具有 **givenName**、 **姓氏** 和 **streetAddress** 等屬性。</span><span class="sxs-lookup"><span data-stu-id="d2553-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="d2553-108">類別的屬性清單會分成該類別的物件必須包含的屬性，以及物件可能包含的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="d2553-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="d2553-109">目錄會排列在階層中;每個類別的定義也會列出其物件可以是指定類別之物件父系的類別，這會控制目錄階層的形狀。</span><span class="sxs-lookup"><span data-stu-id="d2553-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="d2553-110">架構也會正式定義每個屬性。</span><span class="sxs-lookup"><span data-stu-id="d2553-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="d2553-111">每個屬性的定義都包含屬性的唯一識別碼、屬性的語法 (也就是屬性值的資料類型) 、屬性值的選擇性範圍限制、屬性（attribute）是否只能有一個值或多個值，以及屬性是否已編制索引。</span><span class="sxs-lookup"><span data-stu-id="d2553-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="d2553-112">目錄架構會定義每個屬性一次，而物件類別定義包含架構中所定義之屬性的參考。</span><span class="sxs-lookup"><span data-stu-id="d2553-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="d2553-113">例如，"description" 屬性只會定義一次，而且會由許多物件類別參考。</span><span class="sxs-lookup"><span data-stu-id="d2553-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="d2553-114">這與關係資料庫架構不同，它會針對每個資料表個別定義「屬性」 (資料行) 。</span><span class="sxs-lookup"><span data-stu-id="d2553-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




