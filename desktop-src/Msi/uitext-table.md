---
description: UIText 資料表包含使用者介面中使用之部分字串的當地語系化版本。 這些字串不是任何其他資料表的一部分。 UIText 資料表適用于任何其他資料表中沒有邏輯位置的字串。
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: UIText 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111984"
---
# <a name="uitext-table"></a><span data-ttu-id="351b4-105">UIText 資料表</span><span class="sxs-lookup"><span data-stu-id="351b4-105">UIText Table</span></span>

<span data-ttu-id="351b4-106">UIText 資料表包含使用者介面中使用之部分字串的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="351b4-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="351b4-107">這些字串不是任何其他資料表的一部分。</span><span class="sxs-lookup"><span data-stu-id="351b4-107">These strings are not part of any other table.</span></span> <span data-ttu-id="351b4-108">UIText 資料表適用于任何其他資料表中沒有邏輯位置的字串。</span><span class="sxs-lookup"><span data-stu-id="351b4-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="351b4-109">UIText 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="351b4-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="351b4-110">Column</span><span class="sxs-lookup"><span data-stu-id="351b4-110">Column</span></span> | <span data-ttu-id="351b4-111">類型</span><span class="sxs-lookup"><span data-stu-id="351b4-111">Type</span></span>                         | <span data-ttu-id="351b4-112">答案</span><span class="sxs-lookup"><span data-stu-id="351b4-112">Key</span></span> | <span data-ttu-id="351b4-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="351b4-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="351b4-114">答案</span><span class="sxs-lookup"><span data-stu-id="351b4-114">Key</span></span>    | [<span data-ttu-id="351b4-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="351b4-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="351b4-116">Y</span><span class="sxs-lookup"><span data-stu-id="351b4-116">Y</span></span>   | <span data-ttu-id="351b4-117">N</span><span class="sxs-lookup"><span data-stu-id="351b4-117">N</span></span>        |
| <span data-ttu-id="351b4-118">Text</span><span class="sxs-lookup"><span data-stu-id="351b4-118">Text</span></span>   | [<span data-ttu-id="351b4-119">Text</span><span class="sxs-lookup"><span data-stu-id="351b4-119">Text</span></span>](text.md)             | <span data-ttu-id="351b4-120">N</span><span class="sxs-lookup"><span data-stu-id="351b4-120">N</span></span>   | <span data-ttu-id="351b4-121">Y</span><span class="sxs-lookup"><span data-stu-id="351b4-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="351b4-122">資料行</span><span class="sxs-lookup"><span data-stu-id="351b4-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="351b4-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>關鍵</span><span class="sxs-lookup"><span data-stu-id="351b4-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="351b4-124">識別特定字串的唯一索引鍵。</span><span class="sxs-lookup"><span data-stu-id="351b4-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="351b4-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="351b4-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="351b4-126">字串的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="351b4-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="351b4-127">備註</span><span class="sxs-lookup"><span data-stu-id="351b4-127">Remarks</span></span>

<span data-ttu-id="351b4-128">某些控制項使用 UIText 資料表作為字串的來源。</span><span class="sxs-lookup"><span data-stu-id="351b4-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="351b4-129">如需此表中每個特定控制項所需之字串的相關資訊，請參閱 [消費者介面參考](user-interface-reference.md)中的個別控制項。</span><span class="sxs-lookup"><span data-stu-id="351b4-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="351b4-130">驗證</span><span class="sxs-lookup"><span data-stu-id="351b4-130">Validation</span></span>

<dl>

[<span data-ttu-id="351b4-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="351b4-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="351b4-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="351b4-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



