---
title: 物件 (DS-DN) 語法
description: 包含辨別名稱 (DN) 的字串。
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- 物件 (DS-DN) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104509500"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="1b12c-104">物件 (DS-DN) 語法</span><span class="sxs-lookup"><span data-stu-id="1b12c-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="1b12c-105">包含辨別名稱 (DN) 的字串。</span><span class="sxs-lookup"><span data-stu-id="1b12c-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="1b12c-106">若為具有此語法的屬性，Active Directory 會將屬性值處理為 DN 所識別之物件的參考，並在物件移動或重新命名時自動更新該值。</span><span class="sxs-lookup"><span data-stu-id="1b12c-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="1b12c-107">針對在篩選中包含 DN 語法屬性的查詢，請指定完整的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="1b12c-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="1b12c-108">萬用字元 (例如，cn = John \*) 不受支援。</span><span class="sxs-lookup"><span data-stu-id="1b12c-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="1b12c-109">進入</span><span class="sxs-lookup"><span data-stu-id="1b12c-109">Entry</span></span> | <span data-ttu-id="1b12c-110">值</span><span class="sxs-lookup"><span data-stu-id="1b12c-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="1b12c-111">名稱</span><span class="sxs-lookup"><span data-stu-id="1b12c-111">Name</span></span>         | <span data-ttu-id="1b12c-112">Object(DS-DN)</span><span class="sxs-lookup"><span data-stu-id="1b12c-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="1b12c-113">語法識別碼</span><span class="sxs-lookup"><span data-stu-id="1b12c-113">Syntax ID</span></span>    | <span data-ttu-id="1b12c-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="1b12c-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="1b12c-115">OM 識別碼</span><span class="sxs-lookup"><span data-stu-id="1b12c-115">OM ID</span></span>        | <span data-ttu-id="1b12c-116">127</span><span class="sxs-lookup"><span data-stu-id="1b12c-116">127</span></span>                                                                    |
| <span data-ttu-id="1b12c-117">MAPI 類型</span><span class="sxs-lookup"><span data-stu-id="1b12c-117">MAPI Type</span></span>    | <span data-ttu-id="1b12c-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="1b12c-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="1b12c-119">ADS 類型</span><span class="sxs-lookup"><span data-stu-id="1b12c-119">ADS Type</span></span>     | <span data-ttu-id="1b12c-120">ADSTYPE \_ DN \_ 字串</span><span class="sxs-lookup"><span data-stu-id="1b12c-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="1b12c-121">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="1b12c-121">Variant Type</span></span> | <span data-ttu-id="1b12c-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="1b12c-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="1b12c-123">SDS 類型</span><span class="sxs-lookup"><span data-stu-id="1b12c-123">SDS Type</span></span>     | [<span data-ttu-id="1b12c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1b12c-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="1b12c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b12c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b12c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1b12c-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
