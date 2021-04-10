---
description: 如果設定靜態文字控制項的這個位，控制項會自動嘗試將顯示的文字格式化為代表位元組計數的數位。
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: FormatSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191865"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="694d9-103">FormatSize 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="694d9-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="694d9-104">如果設定靜態文字控制項的這個位，控制項會自動嘗試將顯示的文字格式化為代表位元組計數的數位。</span><span class="sxs-lookup"><span data-stu-id="694d9-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="694d9-105">若要進行適當的格式設定，必須將控制項的文字設定為代表以512位元組單位表示之數位的字串。</span><span class="sxs-lookup"><span data-stu-id="694d9-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="694d9-106">然後，顯示的值會以 kb 為單位來格式化 (KB) 、mb (MB) 或 gb (GB) ，並以代表單位的適當字串顯示。</span><span class="sxs-lookup"><span data-stu-id="694d9-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="694d9-107">如需詳細資訊，請參閱 [文字控制項](text-control.md)。</span><span class="sxs-lookup"><span data-stu-id="694d9-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="694d9-108">原始文字的數值</span><span class="sxs-lookup"><span data-stu-id="694d9-108">Numerical value of original text</span></span> | <span data-ttu-id="694d9-109">使用的單元字串</span><span class="sxs-lookup"><span data-stu-id="694d9-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="694d9-110">小於20480</span><span class="sxs-lookup"><span data-stu-id="694d9-110">Less than 20480</span></span>                  | <span data-ttu-id="694d9-111">KB</span><span class="sxs-lookup"><span data-stu-id="694d9-111">KB</span></span>               |
| <span data-ttu-id="694d9-112">小於20971520</span><span class="sxs-lookup"><span data-stu-id="694d9-112">Less than 20971520</span></span>               | <span data-ttu-id="694d9-113">MB</span><span class="sxs-lookup"><span data-stu-id="694d9-113">MB</span></span>               |
| <span data-ttu-id="694d9-114">小於10737418240</span><span class="sxs-lookup"><span data-stu-id="694d9-114">Less than 10737418240</span></span>            | <span data-ttu-id="694d9-115">GB</span><span class="sxs-lookup"><span data-stu-id="694d9-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="694d9-116">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="694d9-116">Valid Controls</span></span>



| <span data-ttu-id="694d9-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="694d9-117">Decimal</span></span> | <span data-ttu-id="694d9-118">十六進位</span><span class="sxs-lookup"><span data-stu-id="694d9-118">Hexadecimal</span></span> | <span data-ttu-id="694d9-119">控制</span><span class="sxs-lookup"><span data-stu-id="694d9-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="694d9-120">524288</span><span class="sxs-lookup"><span data-stu-id="694d9-120">524288</span></span>  | <span data-ttu-id="694d9-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="694d9-121">0x00080000</span></span>  | <span data-ttu-id="694d9-122">msidbControlAttributesFormatSize</span><span class="sxs-lookup"><span data-stu-id="694d9-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="694d9-123">備註</span><span class="sxs-lookup"><span data-stu-id="694d9-123">Remarks</span></span>

<span data-ttu-id="694d9-124">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FormatSize 位。</span><span class="sxs-lookup"><span data-stu-id="694d9-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="694d9-125">控制項的文字必須設定為代表以512位元組單位表示之數位的字串。</span><span class="sxs-lookup"><span data-stu-id="694d9-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="694d9-126">單元字串的文字定義于 [UIText 資料表](uitext-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="694d9-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="694d9-127">單元字串的位置是由 [**LeftUnit**](leftunit.md) 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="694d9-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="694d9-128">如果 **LeftUnit** 屬性定義為任何值，則單元字串會出現在數值之前。</span><span class="sxs-lookup"><span data-stu-id="694d9-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="694d9-129">如果與控制項相關聯的文字中出現數位字元以外的任何內容，則顯示的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="694d9-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="694d9-130">在執行時間，安裝程式會將 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) 屬性解析為安裝所需的位元組總數（以512為單位）。</span><span class="sxs-lookup"><span data-stu-id="694d9-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="694d9-131">具有 FormatSize 位的靜態文字控制項可以用來自動格式化及標記安裝所需的位元組總數（以 KB、MB 或 GB 為單位）。</span><span class="sxs-lookup"><span data-stu-id="694d9-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="694d9-132">基於此範例的目的，假設總位元組數為18336768。</span><span class="sxs-lookup"><span data-stu-id="694d9-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="694d9-133">安裝程式會將 PrimaryVolumeSpaceRequired 屬性的值設定為18336768除以512或35814。</span><span class="sxs-lookup"><span data-stu-id="694d9-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="694d9-134">文字控制項使用 FormatSize 顯示的數位會是17MB。</span><span class="sxs-lookup"><span data-stu-id="694d9-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="694d9-135">原始文字的數值會以512的單位來提供。</span><span class="sxs-lookup"><span data-stu-id="694d9-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="694d9-136">在上表中，字串20480對應至 KB 字串，因為20480次512會產生10485760位元組或 10240 KB 的結果。</span><span class="sxs-lookup"><span data-stu-id="694d9-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="694d9-137">上表所列的單位字串參考 [UIText 資料表](uitext-table.md)中的索引鍵，其中定義了單元字串的文字。</span><span class="sxs-lookup"><span data-stu-id="694d9-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="694d9-138">單元字串的位置是由 [**LeftUnit**](leftunit.md) 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="694d9-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="694d9-139">如果 **LeftUnit** 屬性定義為任何值，則單元字串會出現在數值之前。</span><span class="sxs-lookup"><span data-stu-id="694d9-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="694d9-140">如果與控制項相關聯的文字中出現數位字元以外的任何內容，則顯示的值為未定義。</span><span class="sxs-lookup"><span data-stu-id="694d9-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="694d9-141">如需詳細資訊，請參閱 [控制屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="694d9-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



