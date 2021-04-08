---
title: String. Symbol 屬性
description: 表示字串資源的名稱。
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- String 符號屬性 Windows 功能區
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843172"
---
# <a name="stringsymbol-property"></a><span data-ttu-id="91c78-104">String. Symbol 屬性</span><span class="sxs-lookup"><span data-stu-id="91c78-104">String.Symbol property</span></span>

<span data-ttu-id="91c78-105">表示字串資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="91c78-105">Represents the name of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="91c78-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="91c78-106">Usage</span></span>

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="91c78-107">屬性</span><span class="sxs-lookup"><span data-stu-id="91c78-107">Attributes</span></span>

<span data-ttu-id="91c78-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="91c78-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="91c78-109">子元素</span><span class="sxs-lookup"><span data-stu-id="91c78-109">Child elements</span></span>

<span data-ttu-id="91c78-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="91c78-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="91c78-111">父元素</span><span class="sxs-lookup"><span data-stu-id="91c78-111">Parent elements</span></span>



| <span data-ttu-id="91c78-112">元素</span><span class="sxs-lookup"><span data-stu-id="91c78-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="91c78-113">**字串**</span><span class="sxs-lookup"><span data-stu-id="91c78-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="91c78-114">備註</span><span class="sxs-lookup"><span data-stu-id="91c78-114">Remarks</span></span>

<span data-ttu-id="91c78-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="91c78-115">Optional.</span></span>

<span data-ttu-id="91c78-116">每個 [**字串**](windowsribbon-element-string.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="91c78-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="91c78-117">符號會與功能區標頭檔中的字串定義相關聯，例如 `#define strSave 59999` 。</span><span class="sxs-lookup"><span data-stu-id="91c78-117">The symbol is associated with a string definition in the Ribbon header file, for example, `#define strSave 59999`.</span></span>

<span data-ttu-id="91c78-118">這個元素包含 *xs： string* 類型的值。</span><span class="sxs-lookup"><span data-stu-id="91c78-118">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="91c78-119">此值受限於包含字母或底線的字串，後面接著字母、數位或底線的任何序列。</span><span class="sxs-lookup"><span data-stu-id="91c78-119">The value is constrained to a string composed of a letter or underscore followed by any sequence of letters, digits, or underscores.</span></span>

<span data-ttu-id="91c78-120">長度上限為100個字元。</span><span class="sxs-lookup"><span data-stu-id="91c78-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="91c78-121">範例</span><span class="sxs-lookup"><span data-stu-id="91c78-121">Examples</span></span>

<span data-ttu-id="91c78-122">下列範例會示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 元素的標記，並以 **字串符號** 宣告。</span><span class="sxs-lookup"><span data-stu-id="91c78-122">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Symbol** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="91c78-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="91c78-123">Requirements</span></span>



| <span data-ttu-id="91c78-124">需求</span><span class="sxs-lookup"><span data-stu-id="91c78-124">Requirement</span></span> | <span data-ttu-id="91c78-125">值</span><span class="sxs-lookup"><span data-stu-id="91c78-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="91c78-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91c78-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91c78-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91c78-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="91c78-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91c78-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91c78-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91c78-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





