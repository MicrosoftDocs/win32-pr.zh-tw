---
title: CPRPOBJ.Cpp
description: 在範例提供者元件中，屬性物件方法（在 cprpobj 中）會列在下表中。
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182994"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="8c4fd-103">CPRPOBJ.Cpp</span><span class="sxs-lookup"><span data-stu-id="8c4fd-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="8c4fd-104">在範例提供者元件中，屬性物件方法（在 cprpobj 中）會列在下表中。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="8c4fd-105">方法</span><span class="sxs-lookup"><span data-stu-id="8c4fd-105">Method</span></span>                                                 | <span data-ttu-id="8c4fd-106">描述</span><span class="sxs-lookup"><span data-stu-id="8c4fd-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4fd-107">**CSampleDSProperty::CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="8c4fd-108">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="8c4fd-109">**CSampleDSProperty：： ~ CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="8c4fd-110">標準的函式。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="8c4fd-111">**CSampleDSProperty：： CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="8c4fd-112">建立 ADS 屬性物件，藉由呼叫 **SampleDSGetPropertyDefinition** 來查閱屬性定義。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="8c4fd-113">**CSampleDSProperty：： CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="8c4fd-114">在指定屬性定義的情況下，建立屬性物件，並設定支援的 ADS 語法與提供者語法之間的對應。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="8c4fd-115">**CSampleDSProperty::AllocatePropertyObject**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="8c4fd-116">建立屬性物件並載入其類型資料。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="8c4fd-117">**CSampleDSProperty：： QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="8c4fd-118">傳回要求的介面指標（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="8c4fd-119">標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 方法。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="8c4fd-120">標準 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) 方法。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="8c4fd-121">**MapSyntaxIdtoADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="8c4fd-122">設定語法識別碼和 ADS 語法之間的對應。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="8c4fd-123">**MapSyntaxIdtoSampleDSSyntax**</span><span class="sxs-lookup"><span data-stu-id="8c4fd-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="8c4fd-124">設定語法識別碼與提供者語法之間的對應。</span><span class="sxs-lookup"><span data-stu-id="8c4fd-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




