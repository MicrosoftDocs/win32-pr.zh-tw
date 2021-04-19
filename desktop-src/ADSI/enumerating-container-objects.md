---
title: 列舉容器物件
description: 依照慣例，ADSI 中列舉的所有專案都必須是相同的 Automation 資料類型。 例如，列舉不應將某些專案傳回為 VT I4 型別的變數 \_ ，而其他專案則為 vt BSTR 類型的變異 \_ 。
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968820"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="e73d4-104">列舉容器物件</span><span class="sxs-lookup"><span data-stu-id="e73d4-104">Enumerating Container Objects</span></span>

<span data-ttu-id="e73d4-105">依照慣例，ADSI 中列舉的所有專案都必須是相同的 Automation 資料類型。</span><span class="sxs-lookup"><span data-stu-id="e73d4-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="e73d4-106">例如，列舉不應將某些專案傳回為 **vt \_ I4** 型別的 **變數**，而其他專案則為 **vt \_ BSTR** 類型的 **變異**。</span><span class="sxs-lookup"><span data-stu-id="e73d4-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="e73d4-107">為了列舉物件所維護的專案清單，用戶端會要求針對所列出的特定資訊類型建立列舉物件。</span><span class="sxs-lookup"><span data-stu-id="e73d4-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="e73d4-108">在 ADSI 中，用戶端可能會列出命名空間物件、泛型容器物件、集合物件、成員物件或架構物件中的物件。</span><span class="sxs-lookup"><span data-stu-id="e73d4-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="e73d4-109">ADSI 提供的篩選準則可以設定和修改，以限制任何列舉中的相符專案，但 [**IADsContainer. filter**](iadscontainer-property-methods.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e73d4-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="e73d4-110">您可以在下列 ADs 容器物件的範例提供者元件程式碼中找到列舉值物件的範例。</span><span class="sxs-lookup"><span data-stu-id="e73d4-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="e73d4-111">物件型別</span><span class="sxs-lookup"><span data-stu-id="e73d4-111">Object type</span></span>         | <span data-ttu-id="e73d4-112">code</span><span class="sxs-lookup"><span data-stu-id="e73d4-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="e73d4-113">一般容器</span><span class="sxs-lookup"><span data-stu-id="e73d4-113">Generic Container</span></span>   | <span data-ttu-id="e73d4-114">cenumobj .cpp</span><span class="sxs-lookup"><span data-stu-id="e73d4-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="e73d4-115">命名空間容器</span><span class="sxs-lookup"><span data-stu-id="e73d4-115">Namespace Container</span></span> | <span data-ttu-id="e73d4-116">cenumns .cpp</span><span class="sxs-lookup"><span data-stu-id="e73d4-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="e73d4-117">架構容器</span><span class="sxs-lookup"><span data-stu-id="e73d4-117">Schema Container</span></span>    | <span data-ttu-id="e73d4-118">cenumsch .cpp</span><span class="sxs-lookup"><span data-stu-id="e73d4-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="e73d4-119">如需用戶端資訊，請參閱 [集合和群組](collections-and-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="e73d4-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




