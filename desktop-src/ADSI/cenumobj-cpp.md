---
title: CENUMOBJ.Cpp
description: 在範例提供者元件中，容器物件的列舉會使用下表所列的 cenumobj 中的常式。
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683081"
---
# <a name="cenumobjcpp"></a><span data-ttu-id="1fd0e-103">CENUMOBJ.Cpp</span><span class="sxs-lookup"><span data-stu-id="1fd0e-103">CENUMOBJ.CPP</span></span>

<span data-ttu-id="1fd0e-104">在範例提供者元件中，容器物件的列舉會使用下表所列的 cenumobj 中的常式。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-104">In the example provider component, the enumeration of a container object uses the routines, from cenumobj.cpp, listed in the following table.</span></span>



| <span data-ttu-id="1fd0e-105">方法</span><span class="sxs-lookup"><span data-stu-id="1fd0e-105">Method</span></span>                                                 | <span data-ttu-id="1fd0e-106">描述</span><span class="sxs-lookup"><span data-stu-id="1fd0e-106">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd0e-107">**CSampleDSGenObjectEnum：： Create**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-107">**CSampleDSGenObjectEnum::Create**</span></span>                     | <span data-ttu-id="1fd0e-108">建立物件，以啟用泛型 Active Directory 物件的列舉。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-108">Create an object to enable enumeration of generic Active Directory objects.</span></span>                                                                                           |
| <span data-ttu-id="1fd0e-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-109">**CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**</span></span>     | <span data-ttu-id="1fd0e-110">初始化。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-110">Initialization.</span></span>                                                                                                                                                       |
| <span data-ttu-id="1fd0e-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-111">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="1fd0e-112">管理物件的抓取。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-112">Manage retrieval of objects.</span></span>                                                                                                                                          |
| <span data-ttu-id="1fd0e-113">**CSampleDSGenObjectEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-113">**CSampleDSGenObjectEnum::FetchObjects**</span></span>               | <span data-ttu-id="1fd0e-114">取出符合篩選準則的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標集合。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-114">Retrieve the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers that match the filter.</span></span>                                                             |
| <span data-ttu-id="1fd0e-115">**CSampleDSGenObjectEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-115">**CSampleDSGenObjectEnum::FetchNextObject**</span></span>            | <span data-ttu-id="1fd0e-116">取得物件，並比對篩選。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-116">Retrieve an object and match against the filter.</span></span> <span data-ttu-id="1fd0e-117">如果相符，請將其包裝在泛型物件中，並傳回 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-117">If it matches, wrap it in generic object and return a [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |
| <span data-ttu-id="1fd0e-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-118">**CSampleDSGenObjectEnum::EnumGenericObjects**</span></span>         | <span data-ttu-id="1fd0e-119">管理物件的取出。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-119">Manage retrieving the objects.</span></span>                                                                                                                                        |
| <span data-ttu-id="1fd0e-120">**CSampleDSGenObjectEnum：： Next**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-120">**CSampleDSGenObjectEnum::Next**</span></span>                       | <span data-ttu-id="1fd0e-121">從指出的列舉物件取出指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-121">Retrieve the specified number of elements from the enumeration object indicated.</span></span>                                                                                      |
| <span data-ttu-id="1fd0e-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-122">**CSampleDSGenObjectEnum::IsValidDSFilter**</span></span>            | <span data-ttu-id="1fd0e-123">確認物件類別符合篩選清單中的一個。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-123">Verify that object class matches one in the filter list.</span></span>                                                                                                              |
| <span data-ttu-id="1fd0e-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-124">**CSampleDSGenObjectEnum::BuildDSFilterArray**</span></span>         | <span data-ttu-id="1fd0e-125">管理篩選陣列。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-125">Manage the filter array.</span></span>                                                                                                                                              |
| <span data-ttu-id="1fd0e-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-126">**CSampleDSGenObjectEnum::CreateAndAppendFilterEntry**</span></span> | <span data-ttu-id="1fd0e-127">將新的物件類別加入至篩選，並將篩選準則設定為連續。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-127">Add a new object class to the filter and set the filter as contiguous.</span></span>                                                                                                |
| <span data-ttu-id="1fd0e-128">**FreeFilterList**</span><span class="sxs-lookup"><span data-stu-id="1fd0e-128">**FreeFilterList**</span></span>                                     | <span data-ttu-id="1fd0e-129">釋放篩選。</span><span class="sxs-lookup"><span data-stu-id="1fd0e-129">Free the filter.</span></span>                                                                                                                                                      |



 

 

 