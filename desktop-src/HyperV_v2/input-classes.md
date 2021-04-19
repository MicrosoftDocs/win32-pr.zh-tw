---
description: 使用者輸入裝置是由這些類別表示。 虛擬機器一律會有一個與其相關聯之類別的實例。
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: 輸入類別
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979052"
---
# <a name="input-classes"></a><span data-ttu-id="fa9bd-104">輸入類別</span><span class="sxs-lookup"><span data-stu-id="fa9bd-104">Input classes</span></span>

<span data-ttu-id="fa9bd-105">使用者輸入裝置是由這些類別表示。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="fa9bd-106">虛擬機器一律會有一個與其相關聯之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="fa9bd-107">這些裝置可能不會在虛擬機器中新增或移除。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="fa9bd-108">因此，鍵盤或滑鼠裝置沒有資源集區實例。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="fa9bd-109">鍵盤和滑鼠裝置會透過 [**Msvm \_ SystemDevice**](msvm-systemdevice.md) 關聯連結到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="fa9bd-110">虛擬機器包含 PS2 和綜合滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="fa9bd-111">一次只能有一個作用中的指向裝置。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="fa9bd-112">以下是與輸入相關的虛擬化 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa9bd-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="fa9bd-113">In this section</span></span>



| <span data-ttu-id="fa9bd-114">主題</span><span class="sxs-lookup"><span data-stu-id="fa9bd-114">Topic</span></span>                                                          | <span data-ttu-id="fa9bd-115">描述</span><span class="sxs-lookup"><span data-stu-id="fa9bd-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="fa9bd-116">**Msvm \_ 鍵盤**</span><span class="sxs-lookup"><span data-stu-id="fa9bd-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="fa9bd-117">代表鍵盤裝置。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="fa9bd-118">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="fa9bd-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="fa9bd-119">表示 PS2 滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="fa9bd-120">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="fa9bd-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="fa9bd-121">代表綜合滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="fa9bd-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




