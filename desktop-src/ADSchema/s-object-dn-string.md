---
title: 物件 (DN-字串) 語法
description: 包含字串值和 DN 的八位字串。
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- 物件 (DN-字串) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "106991315"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="dca09-104">物件 (DN-字串) 語法</span><span class="sxs-lookup"><span data-stu-id="dca09-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="dca09-105">包含字串值和 DN 的八位字串。</span><span class="sxs-lookup"><span data-stu-id="dca09-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="dca09-106">進入</span><span class="sxs-lookup"><span data-stu-id="dca09-106">Entry</span></span> | <span data-ttu-id="dca09-107">值</span><span class="sxs-lookup"><span data-stu-id="dca09-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dca09-108">名稱</span><span class="sxs-lookup"><span data-stu-id="dca09-108">Name</span></span>         | <span data-ttu-id="dca09-109">Object(DN-String)</span><span class="sxs-lookup"><span data-stu-id="dca09-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="dca09-110">語法識別碼</span><span class="sxs-lookup"><span data-stu-id="dca09-110">Syntax ID</span></span>    | <span data-ttu-id="dca09-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="dca09-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="dca09-112">OM 識別碼</span><span class="sxs-lookup"><span data-stu-id="dca09-112">OM ID</span></span>        | <span data-ttu-id="dca09-113">127</span><span class="sxs-lookup"><span data-stu-id="dca09-113">127</span></span>                                                                                |
| <span data-ttu-id="dca09-114">MAPI 類型</span><span class="sxs-lookup"><span data-stu-id="dca09-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="dca09-115">ADS 類型</span><span class="sxs-lookup"><span data-stu-id="dca09-115">ADS Type</span></span>     | <span data-ttu-id="dca09-116">\_ \_ 以字串 ADSTYPE \_ DN</span><span class="sxs-lookup"><span data-stu-id="dca09-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="dca09-117">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="dca09-117">Variant Type</span></span> | <span data-ttu-id="dca09-118">VT \_ 分派</span><span class="sxs-lookup"><span data-stu-id="dca09-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="dca09-119">SDS 類型</span><span class="sxs-lookup"><span data-stu-id="dca09-119">SDS Type</span></span>     | <span data-ttu-id="dca09-120">可以轉換成 [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="dca09-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="dca09-121">備註</span><span class="sxs-lookup"><span data-stu-id="dca09-121">Remarks</span></span>

<span data-ttu-id="dca09-122">具有此語法的值具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="dca09-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="dca09-123">其中「 &lt; char count」 &gt; 是「字串值」字串中的字元數 &lt; &gt; ，而「 &lt; 物件 DN」 &gt; 是 Active Directory 中物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="dca09-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="dca09-124">如果移動或重新命名它所參考的物件，Active Directory 會更新 DN。</span><span class="sxs-lookup"><span data-stu-id="dca09-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="dca09-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dca09-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca09-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="dca09-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
