---
title: CENUMNS.Cpp
description: 在範例提供者元件中，命名空間物件的列舉會使用下表所列 cenumns 中的方法。
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969535"
---
# <a name="cenumnscpp"></a><span data-ttu-id="1dd60-103">CENUMNS.Cpp</span><span class="sxs-lookup"><span data-stu-id="1dd60-103">CENUMNS.CPP</span></span>

<span data-ttu-id="1dd60-104">在範例提供者元件中，命名空間物件的列舉會使用下表所列 cenumns 中的方法。</span><span class="sxs-lookup"><span data-stu-id="1dd60-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="1dd60-105">方法</span><span class="sxs-lookup"><span data-stu-id="1dd60-105">Method</span></span>                                              | <span data-ttu-id="1dd60-106">描述</span><span class="sxs-lookup"><span data-stu-id="1dd60-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd60-107">**CSampleDSNamespaceEnum：： Create**</span><span class="sxs-lookup"><span data-stu-id="1dd60-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="1dd60-108">建立物件，以允許列舉 ADS 命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="1dd60-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="1dd60-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="1dd60-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="1dd60-110">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="1dd60-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="1dd60-111">**CSampleDSNamespaceEnum：： ~ CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="1dd60-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="1dd60-112">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="1dd60-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="1dd60-113">**CSampleDSNamespaceEnum：： Next**</span><span class="sxs-lookup"><span data-stu-id="1dd60-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="1dd60-114">從指定的命名空間物件取出指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="1dd60-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="1dd60-115">**CSampleDSNamespaceEnum：： EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="1dd60-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="1dd60-116">管理物件介面指標的取出。</span><span class="sxs-lookup"><span data-stu-id="1dd60-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="1dd60-117">**CSampleDSNamespaceEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="1dd60-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="1dd60-118">提取 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標集合。</span><span class="sxs-lookup"><span data-stu-id="1dd60-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="1dd60-119">**CSampleDSNamespaceEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="1dd60-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="1dd60-120">提取下一個物件。</span><span class="sxs-lookup"><span data-stu-id="1dd60-120">Fetch the next object.</span></span> <span data-ttu-id="1dd60-121">如果找到，請建立泛型 Active Directory 物件並取出其 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 指標。</span><span class="sxs-lookup"><span data-stu-id="1dd60-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 