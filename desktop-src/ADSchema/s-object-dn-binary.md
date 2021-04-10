---
title: 物件 (DN-二進位) 語法
description: 包含二進位值的八位字串以及 (DN) 的分辨名稱。
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- 物件 (DN-二進位) 語法 AD 架構
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106703"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="e9c91-104">物件 (DN-二進位) 語法</span><span class="sxs-lookup"><span data-stu-id="e9c91-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="e9c91-105">包含二進位值的八位字串以及 (DN) 的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c91-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="e9c91-106">進入</span><span class="sxs-lookup"><span data-stu-id="e9c91-106">Entry</span></span> | <span data-ttu-id="e9c91-107">值</span><span class="sxs-lookup"><span data-stu-id="e9c91-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c91-108">名稱</span><span class="sxs-lookup"><span data-stu-id="e9c91-108">Name</span></span>         | <span data-ttu-id="e9c91-109">Object(DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="e9c91-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="e9c91-110">語法識別碼</span><span class="sxs-lookup"><span data-stu-id="e9c91-110">Syntax ID</span></span>    | <span data-ttu-id="e9c91-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="e9c91-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="e9c91-112">OM 識別碼</span><span class="sxs-lookup"><span data-stu-id="e9c91-112">OM ID</span></span>        | <span data-ttu-id="e9c91-113">127</span><span class="sxs-lookup"><span data-stu-id="e9c91-113">127</span></span>                                                                                |
| <span data-ttu-id="e9c91-114">MAPI 類型</span><span class="sxs-lookup"><span data-stu-id="e9c91-114">MAPI Type</span></span>    | <span data-ttu-id="e9c91-115">TSTRING</span><span class="sxs-lookup"><span data-stu-id="e9c91-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="e9c91-116">ADS 類型</span><span class="sxs-lookup"><span data-stu-id="e9c91-116">ADS Type</span></span>     | <span data-ttu-id="e9c91-117">\_ \_ 使用二進位 ADSTYPE \_ DN</span><span class="sxs-lookup"><span data-stu-id="e9c91-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="e9c91-118">Variant 類型</span><span class="sxs-lookup"><span data-stu-id="e9c91-118">Variant Type</span></span> | <span data-ttu-id="e9c91-119">VT \_ 分派</span><span class="sxs-lookup"><span data-stu-id="e9c91-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="e9c91-120">SDS 類型</span><span class="sxs-lookup"><span data-stu-id="e9c91-120">SDS Type</span></span>     | <span data-ttu-id="e9c91-121">可以轉換成 [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="e9c91-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="e9c91-122">備註</span><span class="sxs-lookup"><span data-stu-id="e9c91-122">Remarks</span></span>

<span data-ttu-id="e9c91-123">具有此語法的值具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="e9c91-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="e9c91-124">其中「 &lt; char count」 &gt; 是「二進位值」中的十六進位數位數目 &lt; ，「 &gt; &lt; 二進位值」 &gt; 是二進位值的十六進位標記法，而「 &lt; 物件 DN」 &gt; 是辨別名稱。</span><span class="sxs-lookup"><span data-stu-id="e9c91-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="e9c91-125">如果移動或重新命名它所參考的物件，Active Directory 會自動更新該 DN。</span><span class="sxs-lookup"><span data-stu-id="e9c91-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="e9c91-126">如需使用此語法的詳細資訊和程式碼範例，請參閱 [使用 OtherWellKnownObjects 屬性啟用重新命名安全](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property)系結。</span><span class="sxs-lookup"><span data-stu-id="e9c91-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="e9c91-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9c91-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c91-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="e9c91-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
