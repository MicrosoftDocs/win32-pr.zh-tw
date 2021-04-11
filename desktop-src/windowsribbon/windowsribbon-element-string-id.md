---
title: String.Id 屬性
description: 表示字串資源的唯一識別碼。
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id 屬性視窗功能區
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105623"
---
# <a name="stringid-property"></a><span data-ttu-id="cf68c-104">String.Id 屬性</span><span class="sxs-lookup"><span data-stu-id="cf68c-104">String.Id property</span></span>

<span data-ttu-id="cf68c-105">表示字串資源的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cf68c-105">Represents the unique ID of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="cf68c-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="cf68c-106">Usage</span></span>

``` syntax
<String.Id/>
```

## <a name="attributes"></a><span data-ttu-id="cf68c-107">屬性</span><span class="sxs-lookup"><span data-stu-id="cf68c-107">Attributes</span></span>

<span data-ttu-id="cf68c-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="cf68c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cf68c-109">子元素</span><span class="sxs-lookup"><span data-stu-id="cf68c-109">Child elements</span></span>

<span data-ttu-id="cf68c-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="cf68c-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="cf68c-111">父元素</span><span class="sxs-lookup"><span data-stu-id="cf68c-111">Parent elements</span></span>



| <span data-ttu-id="cf68c-112">元素</span><span class="sxs-lookup"><span data-stu-id="cf68c-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="cf68c-113">**字串**</span><span class="sxs-lookup"><span data-stu-id="cf68c-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="cf68c-114">備註</span><span class="sxs-lookup"><span data-stu-id="cf68c-114">Remarks</span></span>

<span data-ttu-id="cf68c-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cf68c-115">Optional.</span></span>

<span data-ttu-id="cf68c-116">每個 [**字串**](windowsribbon-element-string.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="cf68c-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="cf68c-117">**String.Id** 的值必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="cf68c-117">The value for **String.Id** must be unique.</span></span>

<span data-ttu-id="cf68c-118">此識別碼與功能區標頭檔中的字串定義相關聯，例如 `#define strSave 59999` 。</span><span class="sxs-lookup"><span data-stu-id="cf68c-118">The ID is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="cf68c-119">這個元素包含類型 *xs： positiveInteger* 和 *xs： string* 等位的值。</span><span class="sxs-lookup"><span data-stu-id="cf68c-119">This element contains a value from the union of types *xs:positiveInteger* and *xs:string*.</span></span> <span data-ttu-id="cf68c-120">值受限於介於2到59999（含）之間的整數值，或以十六進位（含）表示的0xea5f。</span><span class="sxs-lookup"><span data-stu-id="cf68c-120">The value is constrained to a integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span>

<span data-ttu-id="cf68c-121">最大長度為10個字元，選擇性前置零。</span><span class="sxs-lookup"><span data-stu-id="cf68c-121">The maximum length is 10 characters with optional leading zeros.</span></span>

## <a name="examples"></a><span data-ttu-id="cf68c-122">範例</span><span class="sxs-lookup"><span data-stu-id="cf68c-122">Examples</span></span>

<span data-ttu-id="cf68c-123">下列範例示範具有 **String.Id** 宣告的 [**LabelTitle**](windowsribbon-element-command-labeltitle.md)元素標記。</span><span class="sxs-lookup"><span data-stu-id="cf68c-123">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Id** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="cf68c-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf68c-124">Requirements</span></span>



| <span data-ttu-id="cf68c-125">需求</span><span class="sxs-lookup"><span data-stu-id="cf68c-125">Requirement</span></span> | <span data-ttu-id="cf68c-126">值</span><span class="sxs-lookup"><span data-stu-id="cf68c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="cf68c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf68c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf68c-128">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf68c-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="cf68c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf68c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf68c-130">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf68c-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





