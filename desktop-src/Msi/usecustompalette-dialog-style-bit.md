---
description: 如果設定此位，則會使用自訂調色盤來建立對話方塊中的圖片， (從) 建立的第一個控制項收到的每個對話方塊。 如果未設定位，則會使用預設的調色板來呈現圖片。
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: UseCustomPalette 對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985130"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="99ad5-104">UseCustomPalette 對話方塊樣式位</span><span class="sxs-lookup"><span data-stu-id="99ad5-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="99ad5-105">如果設定此位，則會使用自訂調色盤來建立對話方塊中的圖片， (從) 建立的第一個控制項收到的每個對話方塊。</span><span class="sxs-lookup"><span data-stu-id="99ad5-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="99ad5-106">如果未設定位，則會使用預設的調色板來呈現圖片。</span><span class="sxs-lookup"><span data-stu-id="99ad5-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="99ad5-107">如果對話方塊包含具有特殊調色板的圖片或共用自訂調色盤的數張圖片，通常會設定此位。</span><span class="sxs-lookup"><span data-stu-id="99ad5-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="99ad5-108">如果對話方塊包含數個具有不同調色板的圖片，則不應設定此位。</span><span class="sxs-lookup"><span data-stu-id="99ad5-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="99ad5-109">在此情況下，預設的調色板最有可能會對所有圖片提供令人滿意的結果。</span><span class="sxs-lookup"><span data-stu-id="99ad5-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="99ad5-110">值</span><span class="sxs-lookup"><span data-stu-id="99ad5-110">Value</span></span>



| <span data-ttu-id="99ad5-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="99ad5-111">Decimal</span></span> | <span data-ttu-id="99ad5-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="99ad5-112">Hexadecimal</span></span> | <span data-ttu-id="99ad5-113">常數</span><span class="sxs-lookup"><span data-stu-id="99ad5-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="99ad5-114">64</span><span class="sxs-lookup"><span data-stu-id="99ad5-114">64</span></span>      | <span data-ttu-id="99ad5-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="99ad5-115">0x00000040</span></span>  | <span data-ttu-id="99ad5-116">**msidbDialogAttributesUseCustomPalette**</span><span class="sxs-lookup"><span data-stu-id="99ad5-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



