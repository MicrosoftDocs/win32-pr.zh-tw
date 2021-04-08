---
title: CENUMSCH.Cpp
description: 在範例提供者元件中，架構物件的列舉會使用下表所列 cenumsch 中的方法。
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839228"
---
# <a name="cenumschcpp"></a><span data-ttu-id="71186-103">CENUMSCH.Cpp</span><span class="sxs-lookup"><span data-stu-id="71186-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="71186-104">在範例提供者元件中，架構物件的列舉會使用下表所列 cenumsch 中的方法。</span><span class="sxs-lookup"><span data-stu-id="71186-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="71186-105">方法</span><span class="sxs-lookup"><span data-stu-id="71186-105">Method</span></span>                                        | <span data-ttu-id="71186-106">描述</span><span class="sxs-lookup"><span data-stu-id="71186-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71186-107">**CSampleDSSchemaEnum：： Create**</span><span class="sxs-lookup"><span data-stu-id="71186-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="71186-108">建立物件以允許 ADSI 架構類別物件的列舉。</span><span class="sxs-lookup"><span data-stu-id="71186-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="71186-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="71186-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="71186-110">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="71186-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="71186-111">**CSampleDSSchemaEnum：： ~ CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="71186-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="71186-112">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="71186-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="71186-113">**CSampleDSSchemaEnum：： Next**</span><span class="sxs-lookup"><span data-stu-id="71186-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="71186-114">從指定的架構物件中取出指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="71186-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="71186-115">**CSampleDSSchemaEnum：： EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="71186-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="71186-116">管理如何抓取介面指標，指向所指定物件類型的物件。</span><span class="sxs-lookup"><span data-stu-id="71186-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="71186-117">**CSampleDSSchemaEnum：： EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="71186-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="71186-118">管理如何抓取預設物件類型之物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="71186-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="71186-119">**CSampleDSSchemaEnum::EnumClasses**</span><span class="sxs-lookup"><span data-stu-id="71186-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="71186-120">管理只抓取此物件中包含之架構類別物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="71186-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="71186-121">**CSampleDSSchemaEnum：： GetClassObject**</span><span class="sxs-lookup"><span data-stu-id="71186-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="71186-122">取出下一個架構類別定義;如果找到，請建立架構類別物件，並傳回介面指標。</span><span class="sxs-lookup"><span data-stu-id="71186-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="71186-123">**CSampleDSSchemaEnum：： EnumProperties**</span><span class="sxs-lookup"><span data-stu-id="71186-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="71186-124">管理將介面指標僅包含在此物件中的屬性物件。</span><span class="sxs-lookup"><span data-stu-id="71186-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="71186-125">**CSampleDSSchemaEnum::GetPropertyObject**</span><span class="sxs-lookup"><span data-stu-id="71186-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="71186-126">取出下一個屬性定義;如果找到，請建立架構類別物件，並傳回介面指標。</span><span class="sxs-lookup"><span data-stu-id="71186-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="71186-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span><span class="sxs-lookup"><span data-stu-id="71186-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="71186-128">管理將介面指標僅包含在此物件中的介面物件。</span><span class="sxs-lookup"><span data-stu-id="71186-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="71186-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span><span class="sxs-lookup"><span data-stu-id="71186-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="71186-130">取出下一個語法定義;如果找到，請建立架構類別物件，並傳回介面指標。</span><span class="sxs-lookup"><span data-stu-id="71186-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




