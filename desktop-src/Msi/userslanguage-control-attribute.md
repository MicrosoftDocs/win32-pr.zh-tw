---
description: 如果設定此位旗標，則會使用使用者的預設 UI 字碼頁來建立字型。 如果未設定位旗標，則會使用資料庫字碼頁來建立字型。
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: UsersLanguage 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977285"
---
# <a name="userslanguage-control-attribute"></a><span data-ttu-id="7f1e1-104">UsersLanguage 控制項屬性</span><span class="sxs-lookup"><span data-stu-id="7f1e1-104">UsersLanguage Control Attribute</span></span>

<span data-ttu-id="7f1e1-105">如果設定此位旗標，則會使用使用者的預設 UI 字碼頁來建立字型。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-105">If this bit flag is set, fonts are created using the user's default UI code page.</span></span> <span data-ttu-id="7f1e1-106">如果未設定位旗標，則會使用資料庫字碼頁來建立字型。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-106">If the bit flag is not set, fonts are created using the database code page.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7f1e1-107">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="7f1e1-107">Valid Controls</span></span>

[<span data-ttu-id="7f1e1-108">Text</span><span class="sxs-lookup"><span data-stu-id="7f1e1-108">Text</span></span>](text-control.md)

 

[<span data-ttu-id="7f1e1-109">ListBox</span><span class="sxs-lookup"><span data-stu-id="7f1e1-109">ListBox</span></span>](listbox-control.md)

 

[<span data-ttu-id="7f1e1-110">ComboBox</span><span class="sxs-lookup"><span data-stu-id="7f1e1-110">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="7f1e1-111">值</span><span class="sxs-lookup"><span data-stu-id="7f1e1-111">Value</span></span>



| <span data-ttu-id="7f1e1-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="7f1e1-112">Decimal</span></span> | <span data-ttu-id="7f1e1-113">十六進位</span><span class="sxs-lookup"><span data-stu-id="7f1e1-113">Hexadecimal</span></span> | <span data-ttu-id="7f1e1-114">常數</span><span class="sxs-lookup"><span data-stu-id="7f1e1-114">Constant</span></span>                                |
|---------|-------------|-----------------------------------------|
| <span data-ttu-id="7f1e1-115">1048576</span><span class="sxs-lookup"><span data-stu-id="7f1e1-115">1048576</span></span> | <span data-ttu-id="7f1e1-116">0x00100000</span><span class="sxs-lookup"><span data-stu-id="7f1e1-116">0x00100000</span></span>  | <span data-ttu-id="7f1e1-117">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="7f1e1-117">**msidbControlAttributesUsersLanguage**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f1e1-118">備註</span><span class="sxs-lookup"><span data-stu-id="7f1e1-118">Remarks</span></span>

<span data-ttu-id="7f1e1-119">這個控制項屬性可以用來顯示使用者已在 [編輯](edit-control.md) 或 [PathEdit](pathedit-control.md) 控制項中輸入的文字。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-119">This control attribute can be used to display text that the user has entered into an [Edit](edit-control.md) or [PathEdit](pathedit-control.md) control.</span></span>

<span data-ttu-id="7f1e1-120">Edit control、PathEdit control、 [DirectoryList control](directorylist-control.md) 和 [DirectoryCombo control](directorycombo-control.md) 一律會使用使用者預設 UI 字碼頁中所建立的字型。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-120">The Edit control, PathEdit control, [DirectoryList control](directorylist-control.md) and [DirectoryCombo control](directorycombo-control.md) always use the fonts created in the user's default UI code page.</span></span> <span data-ttu-id="7f1e1-121">如果作業系統上已安裝其他語言，這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-121">This can cause problems if additional languages have been installed on the operating system.</span></span> <span data-ttu-id="7f1e1-122">在此情況下，電腦上的字型可能無法以新增的語言呈現所有的字元。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-122">In this case, the fonts on the computer may not be able to represent all the characters in the added languages.</span></span> <span data-ttu-id="7f1e1-123">若要判斷可以使用的字型，請查閱 **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SystemLink** 中的值。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-123">To determine what fonts can be used, look up the values in **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\FontLink\\SystemLink**.</span></span>

<span data-ttu-id="7f1e1-124">如需詳細資訊，請參閱 [控制屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="7f1e1-124">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



