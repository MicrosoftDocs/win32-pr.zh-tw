---
title: CommandsWindow 物件
description: CommandsWindow 物件
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967663"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="2246c-103">CommandsWindow 物件</span><span class="sxs-lookup"><span data-stu-id="2246c-103">The CommandsWindow Object</span></span>

<span data-ttu-id="2246c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2246c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="2246c-105">[**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object)物件可讓您存取 [語音命令] 視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="2246c-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="2246c-106">[語音命令] 視窗是一種共用資源，主要是設計來讓使用者能夠查看啟用語音的命令。</span><span class="sxs-lookup"><span data-stu-id="2246c-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="2246c-107">如果已停用 [語音辨識]，[語音命令] 視窗仍會顯示，並以字元) 的語言 (文字「語音輸入已停用」。</span><span class="sxs-lookup"><span data-stu-id="2246c-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="2246c-108">如果未安裝任何符合字元語言設定的語音引擎，則會顯示「無法使用語音輸入」。</span><span class="sxs-lookup"><span data-stu-id="2246c-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="2246c-109">如果輸入-主動用戶端尚未針對其命令定義語音參數，且已停用全域語音命令，則視窗會顯示「沒有聲音命令」。</span><span class="sxs-lookup"><span data-stu-id="2246c-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="2246c-110">您也可以查詢 [語音命令] 視窗的內容，不論語音輸入是否已停用或是否已安裝相容的語音引擎。</span><span class="sxs-lookup"><span data-stu-id="2246c-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="2246c-111">CommandsWindow 屬性</span><span class="sxs-lookup"><span data-stu-id="2246c-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 