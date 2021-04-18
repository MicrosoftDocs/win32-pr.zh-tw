---
title: ADSI 屬性和屬性
description: 屬性（attribute）有時也稱為屬性（property）。 這可能會造成混淆。 本檔會使用下列屬性和屬性定義。
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Adsi 屬性和屬性 ADSI
- ADSI ADSI、使用、存取及運算元據、屬性和屬性
- ADSI 屬性
- 屬性 ADSI
- 屬性 ADSI，已定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965967"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="3b4b7-110">ADSI 屬性和屬性</span><span class="sxs-lookup"><span data-stu-id="3b4b7-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="3b4b7-111">屬性（attribute）有時也稱為屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="3b4b7-112">這可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-112">This can cause confusion.</span></span> <span data-ttu-id="3b4b7-113">本檔會使用下列屬性和屬性定義。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="3b4b7-114">屬性是與程式設計物件相關聯的名稱值。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="3b4b7-115">例如， [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面會公開屬性，例如 [**類別**](iads-property-methods.md) 和 **名稱**。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="3b4b7-116">屬性是與目錄服務中的物件相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="3b4b7-117">例如，使用者物件將會有一個名為 **cn** 的屬性，其中包含的字串是物件的一般或相對分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="3b4b7-118">您可以透過 ADSI 介面方法（例如 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 和 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-put)）來存取屬性。</span><span class="sxs-lookup"><span data-stu-id="3b4b7-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="3b4b7-119">如需 ADSI 屬性和屬性的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="3b4b7-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="3b4b7-120">ADSI 屬性快取</span><span class="sxs-lookup"><span data-stu-id="3b4b7-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="3b4b7-121">Single 與 Multiple Value 屬性</span><span class="sxs-lookup"><span data-stu-id="3b4b7-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="3b4b7-122">Active Directory 操作屬性</span><span class="sxs-lookup"><span data-stu-id="3b4b7-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




