---
title: Command. Symbol 屬性
description: 代表可在外部參考的命令名稱。
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Command. Symbol 屬性 Windows 功能區
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969810"
---
# <a name="commandsymbol-property"></a><span data-ttu-id="395bd-104">Command. Symbol 屬性</span><span class="sxs-lookup"><span data-stu-id="395bd-104">Command.Symbol property</span></span>

<span data-ttu-id="395bd-105">代表可在外部參考的 [**命令**](windowsribbon-element-command.md) 名稱。</span><span class="sxs-lookup"><span data-stu-id="395bd-105">Represents the name of a [**Command**](windowsribbon-element-command.md) that can be referenced externally.</span></span>

## <a name="usage"></a><span data-ttu-id="395bd-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="395bd-106">Usage</span></span>

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a><span data-ttu-id="395bd-107">屬性</span><span class="sxs-lookup"><span data-stu-id="395bd-107">Attributes</span></span>

<span data-ttu-id="395bd-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="395bd-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="395bd-109">子元素</span><span class="sxs-lookup"><span data-stu-id="395bd-109">Child elements</span></span>

<span data-ttu-id="395bd-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="395bd-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="395bd-111">父元素</span><span class="sxs-lookup"><span data-stu-id="395bd-111">Parent elements</span></span>



| <span data-ttu-id="395bd-112">元素</span><span class="sxs-lookup"><span data-stu-id="395bd-112">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="395bd-113">**命令**</span><span class="sxs-lookup"><span data-stu-id="395bd-113">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="395bd-114">備註</span><span class="sxs-lookup"><span data-stu-id="395bd-114">Remarks</span></span>

<span data-ttu-id="395bd-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="395bd-115">Optional.</span></span>

<span data-ttu-id="395bd-116">每個 [**命令**](windowsribbon-element-command.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="395bd-116">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="395bd-117">符號會與功能區標頭檔中的命令定義相關聯，例如 `#define cmdSave 25003 /* Save */` 。</span><span class="sxs-lookup"><span data-stu-id="395bd-117">The symbol is associated with a Command definition in the Ribbon header file, for example, `#define cmdSave 25003 /* Save */`.</span></span>

<span data-ttu-id="395bd-118">這個元素包含 *xs： string* 類型的值。</span><span class="sxs-lookup"><span data-stu-id="395bd-118">This element contains a value of type *xs:string*.</span></span>

<span data-ttu-id="395bd-119">此值受限於包含字母或底線的字串，後面接著字母、數位和底線的任何序列。</span><span class="sxs-lookup"><span data-stu-id="395bd-119">The value is constrained to a string that consists of a letter or underscore followed by any sequence of letters, digits, and underscores.</span></span>

<span data-ttu-id="395bd-120">長度上限為100個字元。</span><span class="sxs-lookup"><span data-stu-id="395bd-120">The maximum length is 100 characters.</span></span>

## <a name="examples"></a><span data-ttu-id="395bd-121">範例</span><span class="sxs-lookup"><span data-stu-id="395bd-121">Examples</span></span>

<span data-ttu-id="395bd-122">下列範例示範 [**命令**](windowsribbon-element-command.md) 專案的標記與 **命令符號** 宣告。</span><span class="sxs-lookup"><span data-stu-id="395bd-122">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Symbol** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="395bd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="395bd-123">Requirements</span></span>



| <span data-ttu-id="395bd-124">需求</span><span class="sxs-lookup"><span data-stu-id="395bd-124">Requirement</span></span> | <span data-ttu-id="395bd-125">值</span><span class="sxs-lookup"><span data-stu-id="395bd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="395bd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="395bd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="395bd-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="395bd-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="395bd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="395bd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="395bd-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="395bd-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





