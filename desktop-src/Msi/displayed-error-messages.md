---
description: 安裝程式函式可能會顯示錯誤訊息對話方塊，並傳回下列任何錯誤。 只有當使用者介面層級為 [完整]、[已縮減] 或 [基本] 層級時，才會顯示錯誤方塊。 如需詳細資訊，請參閱消費者介面層級。
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: 顯示的錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993037"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="8b761-105">顯示的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8b761-105">Displayed Error Messages</span></span>

<span data-ttu-id="8b761-106">[安裝程式](installer-function-reference.md)函式可能會顯示錯誤訊息對話方塊，並傳回下列任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="8b761-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="8b761-107">只有當使用者介面層級為 [完整]、[已縮減] 或 [基本] 層級時，才會顯示錯誤方塊。</span><span class="sxs-lookup"><span data-stu-id="8b761-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="8b761-108">如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。</span><span class="sxs-lookup"><span data-stu-id="8b761-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="8b761-109">安裝程式函數只會顯示下表中的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="8b761-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="8b761-110">針對不在此清單中的錯誤，函式的呼叫端會負責處理錯誤訊息的顯示。</span><span class="sxs-lookup"><span data-stu-id="8b761-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="8b761-111">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8b761-111">Error code</span></span>               | <span data-ttu-id="8b761-112">錯誤</span><span class="sxs-lookup"><span data-stu-id="8b761-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="8b761-113">\_安裝 \_ 暫止時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="8b761-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="8b761-114">安裝已暫停。</span><span class="sxs-lookup"><span data-stu-id="8b761-114">The install was suspended.</span></span>   |
| <span data-ttu-id="8b761-115">\_安裝 \_ USEREXIT 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="8b761-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="8b761-116">使用者已結束安裝。</span><span class="sxs-lookup"><span data-stu-id="8b761-116">The user exited the install.</span></span> |
| <span data-ttu-id="8b761-117">\_安裝 \_ 失敗時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="8b761-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="8b761-118">安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="8b761-118">Install failed.</span></span>              |



 

 

 



