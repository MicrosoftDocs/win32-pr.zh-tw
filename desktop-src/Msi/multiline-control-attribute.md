---
description: 如果此位設定在編輯控制項上，安裝程式會使用垂直捲動條來建立多行編輯控制項。
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: 多行控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192221"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="d0b6e-103">多行控制項屬性</span><span class="sxs-lookup"><span data-stu-id="d0b6e-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="d0b6e-104">如果此位設定在 [編輯控制項](edit-control.md)上，安裝程式會使用垂直捲動條來建立多行編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="d0b6e-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="d0b6e-105">如果未設定此位，則會指定顯示一般編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="d0b6e-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="d0b6e-106">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="d0b6e-106">Valid Controls</span></span>

<span data-ttu-id="d0b6e-107">[編輯控制項](edit-control.md)。</span><span class="sxs-lookup"><span data-stu-id="d0b6e-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="d0b6e-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="d0b6e-108">Decimal</span></span> | <span data-ttu-id="d0b6e-109">十六進位</span><span class="sxs-lookup"><span data-stu-id="d0b6e-109">Hexadecimal</span></span> | <span data-ttu-id="d0b6e-110">常數</span><span class="sxs-lookup"><span data-stu-id="d0b6e-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="d0b6e-111">65536</span><span class="sxs-lookup"><span data-stu-id="d0b6e-111">65536</span></span>   | <span data-ttu-id="d0b6e-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d0b6e-112">0x00010000</span></span>  | <span data-ttu-id="d0b6e-113">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="d0b6e-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d0b6e-114">備註</span><span class="sxs-lookup"><span data-stu-id="d0b6e-114">Remarks</span></span>

<span data-ttu-id="d0b6e-115">若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含多行位。</span><span class="sxs-lookup"><span data-stu-id="d0b6e-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="d0b6e-116">請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。</span><span class="sxs-lookup"><span data-stu-id="d0b6e-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



