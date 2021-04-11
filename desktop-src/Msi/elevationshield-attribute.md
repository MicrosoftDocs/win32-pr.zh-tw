---
description: 這個屬性會將 [使用者帳戶控制] (UAC) 提高許可權圖示 (盾牌圖示) 新增至按鈕控制項。
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: ElevationShield 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115673"
---
# <a name="elevationshield-attribute"></a><span data-ttu-id="3fba7-103">ElevationShield 屬性</span><span class="sxs-lookup"><span data-stu-id="3fba7-103">ElevationShield Attribute</span></span>

<span data-ttu-id="3fba7-104">這個屬性會將 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 提高許可權圖示 (盾牌圖示) 新增至 [按鈕控制項](pushbutton-control.md)。</span><span class="sxs-lookup"><span data-stu-id="3fba7-104">This attribute adds the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon) to the [PushButton control](pushbutton-control.md).</span></span>

<span data-ttu-id="3fba7-105">如果設定此位，且安裝尚未以較 [*高*](e-gly.md) 的許可權執行，則會使用 [ [*使用者帳戶控制*](u-gly.md) ] (UAC) 提高許可權圖示 (盾牌圖示) 建立按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="3fba7-105">If this bit is set, and the installation is not yet running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the [*User Account Control*](u-gly.md) (UAC) elevation icon (shield icon).</span></span>

<span data-ttu-id="3fba7-106">如果設定此位，而且安裝已經以較 [*高*](e-gly.md) 的許可權執行，則會使用其他圖示屬性來建立按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="3fba7-106">If this bit is set, and the installation is already running with [*elevated*](e-gly.md) privileges, the pushbutton control is created using the other icon attributes.</span></span>

<span data-ttu-id="3fba7-107">如果未設定此位，則會使用其他圖示屬性來建立按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="3fba7-107">If this bit is not set, the pushbutton control is created using the other icon attributes.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="3fba7-108">有效的控制項</span><span class="sxs-lookup"><span data-stu-id="3fba7-108">Valid Controls</span></span>

[<span data-ttu-id="3fba7-109">按鈕</span><span class="sxs-lookup"><span data-stu-id="3fba7-109">PushButton</span></span>](pushbutton-control.md)

## <a name="value"></a><span data-ttu-id="3fba7-110">值</span><span class="sxs-lookup"><span data-stu-id="3fba7-110">Value</span></span>



| <span data-ttu-id="3fba7-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="3fba7-111">Decimal</span></span> | <span data-ttu-id="3fba7-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="3fba7-112">Hexadecimal</span></span> | <span data-ttu-id="3fba7-113">常數</span><span class="sxs-lookup"><span data-stu-id="3fba7-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="3fba7-114">8388608</span><span class="sxs-lookup"><span data-stu-id="3fba7-114">8388608</span></span> | <span data-ttu-id="3fba7-115">0x00800000</span><span class="sxs-lookup"><span data-stu-id="3fba7-115">0x00800000</span></span>  | <span data-ttu-id="3fba7-116">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="3fba7-116">**msidbControlAttributesElevationShield**</span></span> |



 

 

 



