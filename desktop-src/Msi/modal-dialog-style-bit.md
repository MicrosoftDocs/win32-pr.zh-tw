---
description: 如果設定此位，則對話方塊是強制回應的，相同應用程式的其他對話方塊無法放在其上方，且對話方塊會在控制項執行時將它保持在執行狀態。
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: 強制回應對話方塊樣式位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513828"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="36491-103">強制回應對話方塊樣式位</span><span class="sxs-lookup"><span data-stu-id="36491-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="36491-104">如果設定此位，則對話方塊是強制回應的，相同應用程式的其他對話方塊無法放在其上方，且對話方塊會在控制項執行時將它保持在執行狀態。</span><span class="sxs-lookup"><span data-stu-id="36491-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="36491-105">如果未設定此位，則對話方塊為非強制回應，相同應用程式的其他對話方塊可能會在其上方移動。</span><span class="sxs-lookup"><span data-stu-id="36491-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="36491-106">建立並顯示非強制回應對話方塊之後，使用者介面會將控制權傳回到安裝程式。</span><span class="sxs-lookup"><span data-stu-id="36491-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="36491-107">然後，安裝程式會定期呼叫使用者介面來更新對話方塊，並讓它有機會處理訊息。</span><span class="sxs-lookup"><span data-stu-id="36491-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="36491-108">完成這項操作之後，控制權會傳回給安裝程式。</span><span class="sxs-lookup"><span data-stu-id="36491-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="36491-109">在嚮導順序中應該不會有非強制回應對話方塊，因為這會將控制權傳回給安裝程式，並提前結束嚮導順序。</span><span class="sxs-lookup"><span data-stu-id="36491-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="36491-110">值</span><span class="sxs-lookup"><span data-stu-id="36491-110">Value</span></span>



| <span data-ttu-id="36491-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="36491-111">Decimal</span></span> | <span data-ttu-id="36491-112">十六進位</span><span class="sxs-lookup"><span data-stu-id="36491-112">Hexadecimal</span></span> | <span data-ttu-id="36491-113">常數</span><span class="sxs-lookup"><span data-stu-id="36491-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="36491-114">2</span><span class="sxs-lookup"><span data-stu-id="36491-114">2</span></span>       | <span data-ttu-id="36491-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36491-115">0x00000002</span></span>  | <span data-ttu-id="36491-116">**msidbDialogAttributesSysModal**</span><span class="sxs-lookup"><span data-stu-id="36491-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 



