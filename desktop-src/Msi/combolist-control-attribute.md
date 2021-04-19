---
description: 如果已在下拉式方塊上設定 ComboList 控制項位，則會以靜態文字欄位取代編輯欄位。 這可防止使用者輸入新的值，而且需要使用者只選擇其中一個預先定義的值。
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: ComboList 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990357"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="7989f-104">ComboList 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="7989f-104">ComboList Control Attribute</span></span>

<span data-ttu-id="7989f-105">如果已在下拉式方塊上設定 ComboList 控制項位，則會以靜態文字欄位取代編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="7989f-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="7989f-106">這可防止使用者輸入新的值，而且需要使用者只選擇其中一個預先定義的值。</span><span class="sxs-lookup"><span data-stu-id="7989f-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="7989f-107">如果未設定此位，下拉式方塊就會有編輯欄位。</span><span class="sxs-lookup"><span data-stu-id="7989f-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7989f-108">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="7989f-108">Valid Controls</span></span>

[<span data-ttu-id="7989f-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="7989f-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="7989f-110">值</span><span class="sxs-lookup"><span data-stu-id="7989f-110">Value</span></span>



| <span data-ttu-id="7989f-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="7989f-111">Decimal</span></span> | <span data-ttu-id="7989f-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="7989f-112">Hexadecimal</span></span> | <span data-ttu-id="7989f-113">Description</span><span class="sxs-lookup"><span data-stu-id="7989f-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="7989f-114">131072</span><span class="sxs-lookup"><span data-stu-id="7989f-114">131072</span></span>  | <span data-ttu-id="7989f-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="7989f-115">0x00020000</span></span>  | <span data-ttu-id="7989f-116">msidbControlAttributesComboList</span><span class="sxs-lookup"><span data-stu-id="7989f-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7989f-117">備註</span><span class="sxs-lookup"><span data-stu-id="7989f-117">Remarks</span></span>

<span data-ttu-id="7989f-118">若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 ComboList 位。</span><span class="sxs-lookup"><span data-stu-id="7989f-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="7989f-119">請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。</span><span class="sxs-lookup"><span data-stu-id="7989f-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



