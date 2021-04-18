---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969051"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="39b8d-103">IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="39b8d-103">IAgentCommandWindow</span></span>

<span data-ttu-id="39b8d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="39b8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="39b8d-105">**IAgentCommandWindow** 定義了一個介面，可讓應用程式設定和查詢 [語音命令] 視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="39b8d-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="39b8d-106">[語音命令] 視窗是一種共用資源，主要是設計來讓使用者能夠查看啟用語音的命令。</span><span class="sxs-lookup"><span data-stu-id="39b8d-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="39b8d-107">如果已停用 [語音辨識]，[語音命令] 視窗仍會顯示，並以字元) 的語言 (文字「語音輸入已停用」。</span><span class="sxs-lookup"><span data-stu-id="39b8d-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="39b8d-108">如果未安裝符合字元語言設定的語音引擎，則視窗會顯示「無法使用語音輸入」。</span><span class="sxs-lookup"><span data-stu-id="39b8d-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="39b8d-109">如果輸入-主動用戶端尚未針對其命令定義語音參數，且已停用全域語音命令，則視窗會顯示「沒有聲音命令」。</span><span class="sxs-lookup"><span data-stu-id="39b8d-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="39b8d-110">您也可以查詢 [語音命令] 視窗的內容，不論語音輸入是否已停用或是否已安裝相容的語音引擎。</span><span class="sxs-lookup"><span data-stu-id="39b8d-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="39b8d-111">**依照 Vtable 順序的方法**</span><span class="sxs-lookup"><span data-stu-id="39b8d-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="39b8d-112">IAgentCommandWindow 方法</span><span class="sxs-lookup"><span data-stu-id="39b8d-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="39b8d-113">Description</span><span class="sxs-lookup"><span data-stu-id="39b8d-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39b8d-114">**SetVisible**</span><span class="sxs-lookup"><span data-stu-id="39b8d-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="39b8d-115">設定 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="39b8d-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="39b8d-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="39b8d-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="39b8d-117">傳回 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性值。</span><span class="sxs-lookup"><span data-stu-id="39b8d-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="39b8d-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="39b8d-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="39b8d-119">傳回語音命令視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="39b8d-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="39b8d-120">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="39b8d-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="39b8d-121">傳回語音命令視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="39b8d-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 




