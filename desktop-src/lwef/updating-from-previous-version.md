---
title: 從舊版更新
description: 從舊版更新
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969438"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="ab0e3-103">從舊版更新</span><span class="sxs-lookup"><span data-stu-id="ab0e3-103">Updating from Previous Version</span></span>

<span data-ttu-id="ab0e3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ab0e3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="ab0e3-105">使用1.5 舊版 Microsoft 代理程式建立和編譯的應用程式，應該在新的2.0 版本下執行，而不需要修改。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="ab0e3-106">[**連接**](connected-property.md)的屬性不能再設為 **False**;已取代的 SpeechInput 物件的某些屬性仍存在，但不再開啟任何值，而且伺服器不會再引發 [**重新開機**](https://www.bing.com/search?q=**Restart**)和 [**關閉**](https://www.bing.com/search?q=**Shutdown**)事件。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="ab0e3-107">但是，如果您將應用程式更新為使用代理程式2.0 控制項，您可能必須修改程式碼。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="ab0e3-108">如果您已安裝2.0 版的 Microsoft 代理程式並載入 Visual Basic 專案，請使用舊版的 Agent 控制項，Visual Basic 包含的選項會自動顯示一則訊息，指出它偵測到新版本的控制項。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="ab0e3-109">為了確保應用程式能正常運作，請一律選擇使用較新的版本。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="ab0e3-110">針對其他程式設計語言 (例如 Microsoft Office 97 VBA) ），您可能必須先移除 1.5 Agent 控制項並儲存您的程式碼，才能更新控制項。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="ab0e3-111">然後，結束程式設計環境、重新開機程式設計環境、重載您的程式碼，然後插入新的控制項。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="ab0e3-112">避免在您要編輯已啟用代理程式1.5 的應用程式之相同程式設計環境的實例中，編輯已啟用代理程式2.0 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="ab0e3-113">某些程式設計環境可能不會處理兩種版本的控制項之間的差異。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="ab0e3-114">安裝代理程式2.0 版之後，您應該能夠在系統上卸載代理程式1.5 版本。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="ab0e3-115">不過，如果代理程式1.5 是透過2.0 版安裝，您可能必須重新安裝2.0。</span><span class="sxs-lookup"><span data-stu-id="ab0e3-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




