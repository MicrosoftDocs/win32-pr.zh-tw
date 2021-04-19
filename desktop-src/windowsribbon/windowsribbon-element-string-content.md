---
title: Content 屬性
description: 表示字串資源的內容。
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- 字串內容視窗功能區
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969968"
---
# <a name="stringcontent-property"></a><span data-ttu-id="49b51-104">Content 屬性</span><span class="sxs-lookup"><span data-stu-id="49b51-104">String.Content property</span></span>

<span data-ttu-id="49b51-105">表示字串資源的內容。</span><span class="sxs-lookup"><span data-stu-id="49b51-105">Represents the content of a string resource.</span></span>

## <a name="usage"></a><span data-ttu-id="49b51-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="49b51-106">Usage</span></span>

``` syntax
<String.Content/>
```

## <a name="attributes"></a><span data-ttu-id="49b51-107">屬性</span><span class="sxs-lookup"><span data-stu-id="49b51-107">Attributes</span></span>

<span data-ttu-id="49b51-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="49b51-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="49b51-109">子元素</span><span class="sxs-lookup"><span data-stu-id="49b51-109">Child elements</span></span>

<span data-ttu-id="49b51-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="49b51-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="49b51-111">父元素</span><span class="sxs-lookup"><span data-stu-id="49b51-111">Parent elements</span></span>



| <span data-ttu-id="49b51-112">元素</span><span class="sxs-lookup"><span data-stu-id="49b51-112">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="49b51-113">**字串**</span><span class="sxs-lookup"><span data-stu-id="49b51-113">**String**</span></span>](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="49b51-114">備註</span><span class="sxs-lookup"><span data-stu-id="49b51-114">Remarks</span></span>

<span data-ttu-id="49b51-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="49b51-115">Optional.</span></span>

<span data-ttu-id="49b51-116">每個 [**字串**](windowsribbon-element-string.md) 元素最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="49b51-116">May occur at most once for each [**String**](windowsribbon-element-string.md) element.</span></span>

<span data-ttu-id="49b51-117">這個元素包含 *xs： string* 類型的值。</span><span class="sxs-lookup"><span data-stu-id="49b51-117">This element contains a value of type *xs:string*.</span></span> <span data-ttu-id="49b51-118">此值受限於由任何字元序列組成的字串，包括空白字元和分行符號字元。</span><span class="sxs-lookup"><span data-stu-id="49b51-118">The value is constrained to a string composed of any sequence of characters, including white space and line-break characters.</span></span>

<span data-ttu-id="49b51-119">長度上限為未系結。</span><span class="sxs-lookup"><span data-stu-id="49b51-119">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="49b51-120">範例</span><span class="sxs-lookup"><span data-stu-id="49b51-120">Examples</span></span>

<span data-ttu-id="49b51-121">下列範例示範 [**LabelTitle**](windowsribbon-element-command-labeltitle.md) 專案的標記，其中包含 **字串. 內容** 宣告。</span><span class="sxs-lookup"><span data-stu-id="49b51-121">The following example demonstrates the markup for a [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) element with a **String.Content** declaration.</span></span>


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a><span data-ttu-id="49b51-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="49b51-122">Requirements</span></span>



| <span data-ttu-id="49b51-123">需求</span><span class="sxs-lookup"><span data-stu-id="49b51-123">Requirement</span></span> | <span data-ttu-id="49b51-124">值</span><span class="sxs-lookup"><span data-stu-id="49b51-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="49b51-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49b51-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49b51-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b51-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="49b51-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49b51-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49b51-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49b51-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





