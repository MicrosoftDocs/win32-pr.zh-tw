---
title: CCLSOBJ.Cpp
description: 在範例提供者元件中，架構類別物件的函式包含在 cclsobj 中。
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968410"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="0509c-104">CCLSOBJ.Cpp</span><span class="sxs-lookup"><span data-stu-id="0509c-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="0509c-105">在範例提供者元件中，架構類別物件的函式包含在 cclsobj 中。</span><span class="sxs-lookup"><span data-stu-id="0509c-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="0509c-106">**CSampleDSClass** 類別是在這個檔案中定義的。</span><span class="sxs-lookup"><span data-stu-id="0509c-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="0509c-107">**CSampleDSClass** 是使用下表所列的方法和屬性來定義的。</span><span class="sxs-lookup"><span data-stu-id="0509c-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="0509c-108">方法</span><span class="sxs-lookup"><span data-stu-id="0509c-108">Method</span></span>                      | <span data-ttu-id="0509c-109">描述</span><span class="sxs-lookup"><span data-stu-id="0509c-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0509c-110">**CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="0509c-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="0509c-111">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="0509c-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="0509c-112">**~ CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="0509c-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="0509c-113">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="0509c-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="0509c-114">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="0509c-114">**CreateClass**</span></span>             | <span data-ttu-id="0509c-115">建立 ADs 架構類別物件。</span><span class="sxs-lookup"><span data-stu-id="0509c-115">Create an ADs schema class object.</span></span> <span data-ttu-id="0509c-116">藉由呼叫 **SampleDSGetClassDefinition** 來查閱屬性定義。</span><span class="sxs-lookup"><span data-stu-id="0509c-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="0509c-117">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="0509c-117">**CreateClass**</span></span>             | <span data-ttu-id="0509c-118">建立架構類別物件，指定屬性定義，設定已知的屬性，例如 [**得到 iadsclass：： MandatoryAttributes**](iadsclass-property-methods.md)中所列的屬性。</span><span class="sxs-lookup"><span data-stu-id="0509c-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="0509c-119">**AllocateClassObject**</span><span class="sxs-lookup"><span data-stu-id="0509c-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="0509c-120">建立架構類別物件，並載入其類型資料。</span><span class="sxs-lookup"><span data-stu-id="0509c-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="0509c-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="0509c-121">**QueryInterface**</span></span>          | <span data-ttu-id="0509c-122">傳回要求的介面指標（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0509c-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="0509c-123">標準 IADs 方法。</span><span class="sxs-lookup"><span data-stu-id="0509c-123">Standard IADs methods.</span></span>      | <span data-ttu-id="0509c-124">此檔案中包含的標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面方法。</span><span class="sxs-lookup"><span data-stu-id="0509c-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="0509c-125">標準得到 iadsclass 方法。</span><span class="sxs-lookup"><span data-stu-id="0509c-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="0509c-126">此檔案中包含的標準 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面方法。</span><span class="sxs-lookup"><span data-stu-id="0509c-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="0509c-127">**CreatePropertyList**</span><span class="sxs-lookup"><span data-stu-id="0509c-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="0509c-128">藉由呼叫 **CreatePropertyEntry**，建立與此架構類別相關聯的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="0509c-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="0509c-129">**CreatePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="0509c-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="0509c-130">在此架構類別中建立一個屬性物件。</span><span class="sxs-lookup"><span data-stu-id="0509c-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="0509c-131">**FreePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="0509c-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="0509c-132">釋放在 **CreatePropertyEntry** 中所做的專案。</span><span class="sxs-lookup"><span data-stu-id="0509c-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="0509c-133">**MakeVariantFromPropList**</span><span class="sxs-lookup"><span data-stu-id="0509c-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="0509c-134">從 **CreatePropertyList** 所建立的屬性清單建立變體陣列。</span><span class="sxs-lookup"><span data-stu-id="0509c-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="0509c-135">可以用於 [**得到 iadsclass：： MandatoryAttributes**](iadsclass-property-methods.md) 的實，依此類推。</span><span class="sxs-lookup"><span data-stu-id="0509c-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




