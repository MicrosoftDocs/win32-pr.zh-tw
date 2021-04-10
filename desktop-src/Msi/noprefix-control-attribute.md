---
description: 如果在文字控制項上設定此位，則文字字串中出現的字元 &\# 0034; &&\# 0034; 會顯示為本身。 如果未設定此位，則 \# 會將文字字串中的字元 &0034; &&\# 0034;）顯示為帶字元字元。
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191862"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="b6d62-104">NoPrefix 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="b6d62-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="b6d62-105">如果在文字控制項上設定此位，則文字字串中出現的字元 "&" 會顯示為本身。</span><span class="sxs-lookup"><span data-stu-id="b6d62-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="b6d62-106">如果未設定此位，則會將文字字串中 "&" 後面的字元顯示為帶底線。</span><span class="sxs-lookup"><span data-stu-id="b6d62-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b6d62-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="b6d62-107">Valid Controls</span></span>

[<span data-ttu-id="b6d62-108">Text</span><span class="sxs-lookup"><span data-stu-id="b6d62-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="b6d62-109">值</span><span class="sxs-lookup"><span data-stu-id="b6d62-109">Value</span></span>



| <span data-ttu-id="b6d62-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="b6d62-110">Decimal</span></span> | <span data-ttu-id="b6d62-111">十六進位</span><span class="sxs-lookup"><span data-stu-id="b6d62-111">Hexadecimal</span></span> | <span data-ttu-id="b6d62-112">常數</span><span class="sxs-lookup"><span data-stu-id="b6d62-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="b6d62-113">131072</span><span class="sxs-lookup"><span data-stu-id="b6d62-113">131072</span></span>  | <span data-ttu-id="b6d62-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="b6d62-114">0x20000</span></span>     | <span data-ttu-id="b6d62-115">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="b6d62-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b6d62-116">備註</span><span class="sxs-lookup"><span data-stu-id="b6d62-116">Remarks</span></span>

<span data-ttu-id="b6d62-117">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 NoPrefix 位。</span><span class="sxs-lookup"><span data-stu-id="b6d62-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="b6d62-118">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="b6d62-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



