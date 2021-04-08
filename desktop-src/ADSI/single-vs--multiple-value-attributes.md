---
title: Single 與 Multiple Value 屬性
description: 可以存在於目錄中的屬性通常會定義在目錄的架構中。
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- single 與 multiple value 屬性 ADSI
- 屬性 ADSI、single 與 multiple value 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020785"
---
# <a name="single-vs-multiple-value-attributes"></a><span data-ttu-id="17350-105">Single 與 Multiple Value 屬性</span><span class="sxs-lookup"><span data-stu-id="17350-105">Single vs. Multiple Value Attributes</span></span>

<span data-ttu-id="17350-106">可以存在於目錄中的屬性通常會定義在目錄的架構中。</span><span class="sxs-lookup"><span data-stu-id="17350-106">The attributes that can exist in a directory are typically defined in the schema for the directory.</span></span> <span data-ttu-id="17350-107">屬性（attribute）的架構定義（attribute）會指定屬性（attribute）的許多特性（attribute），例如資料類型，以及屬性（attribute）的實例是否可以有多個值。</span><span class="sxs-lookup"><span data-stu-id="17350-107">The schema definition of an attribute specifies a number of characteristics of the attribute, such as the data type and whether an instance of the attribute can have multiple values.</span></span>

<span data-ttu-id="17350-108">單一值屬性的實例可以包含單一值。</span><span class="sxs-lookup"><span data-stu-id="17350-108">An instance of a single-valued attribute can contain a single value.</span></span> <span data-ttu-id="17350-109">多重值屬性的實例可以包含單一值或多個值。</span><span class="sxs-lookup"><span data-stu-id="17350-109">An instance of a multivalued attribute can contain either a single value or multiple values.</span></span> <span data-ttu-id="17350-110">Active Directory 不會建立具有空白值的屬性，因為屬性包含有效的值，或不存在於物件上。</span><span class="sxs-lookup"><span data-stu-id="17350-110">Active Directory does not create attributes with empty values—either the attribute contains a valid value or it does not exist on the object.</span></span>

> [!Note]  
> <span data-ttu-id="17350-111">在 Active Directory 和大部分其他 LDAP 伺服器中，多重值屬性中的值順序是未定義的。</span><span class="sxs-lookup"><span data-stu-id="17350-111">In Active Directory and most other LDAP servers, the order of values in a multi-valued attribute is undefined.</span></span> <span data-ttu-id="17350-112">此外，多重值屬性的每個值都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="17350-112">Also, each value of a multi-valued attribute must be unique.</span></span>

 

<span data-ttu-id="17350-113">如果您的目錄支援架構，則 ADSI 通常會載入架構資料，如同 Active Directory 一樣。</span><span class="sxs-lookup"><span data-stu-id="17350-113">ADSI normally loads schema data if your directory supports a schema, as Active Directory does.</span></span> <span data-ttu-id="17350-114">因為 ADSI 知道架構中的屬性語法，所以在存取它時，您不需要指定屬性類型。</span><span class="sxs-lookup"><span data-stu-id="17350-114">Because ADSI knows the syntax of attributes in the schema, you are not required to specify the attribute type when accessing it.</span></span> <span data-ttu-id="17350-115">ADSI 會將屬性值封送處理至架構中定義的適當資料類型。</span><span class="sxs-lookup"><span data-stu-id="17350-115">ADSI marshals attribute values to the appropriate data type as defined in the schema.</span></span>

<span data-ttu-id="17350-116">如果您的目錄沒有架構，請在存取屬性時提供資料類型。</span><span class="sxs-lookup"><span data-stu-id="17350-116">If your directory has no schema, supply the data type when accessing an attribute.</span></span>

> [!Note]  
> <span data-ttu-id="17350-117">Active Directory、Exchange、Windows NT 4.0 和網站伺服器都有架構。</span><span class="sxs-lookup"><span data-stu-id="17350-117">Active Directory, Exchange, Windows NT 4.0, and Site Server all have a schema.</span></span> <span data-ttu-id="17350-118">此外，Active Directory 具有可延伸的架構。</span><span class="sxs-lookup"><span data-stu-id="17350-118">In addition, Active Directory has an extensible schema.</span></span>

 

 

 




