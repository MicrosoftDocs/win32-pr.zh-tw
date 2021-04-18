---
description: 使用之前，請先判斷 Windows Update 代理程式 (WUA) 的版本。
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: 判斷 WUA 的目前版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983400"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="fc223-103">判斷 WUA 的目前版本</span><span class="sxs-lookup"><span data-stu-id="fc223-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="fc223-104">如需更新 WUA 的一般資訊，包括逐步指示，以程式設計方式在應用程式中判斷電腦上執行的 WUA 版本是否符合您的需求，請參閱 [更新 Windows Update 代理程式](updating-the-windows-update-agent.md)。</span><span class="sxs-lookup"><span data-stu-id="fc223-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="fc223-105">在 Windows 7 和 Windows Server 2008 R2 之前的 Windows 版本上，您應該先判斷安裝的 Windows Update 代理程式 (WUA) 版本，再使用它。</span><span class="sxs-lookup"><span data-stu-id="fc223-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="fc223-106">WUA 的目前版本取決於 \\ 目前 Windows 安裝的 System32 子目錄中執行的 Wuaueng.dll 版本。</span><span class="sxs-lookup"><span data-stu-id="fc223-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="fc223-107">如果 Wuaueng.dll 的版本是5.4.3790.1000 版或更新版本，則會安裝 WUA。</span><span class="sxs-lookup"><span data-stu-id="fc223-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="fc223-108">早于5.4.3790.1000 的版本表示安裝了 (SUS) 1.0 的軟體更新服務。</span><span class="sxs-lookup"><span data-stu-id="fc223-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="fc223-109">使用 WUA API 對 su 1.0 進行呼叫時，  \_ \_ \_ 會傳回 WU E AU LEGACYSERVER 的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="fc223-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="fc223-110">您也可以使用 [**IWindowsUpdateAgentInfo：： GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) 方法來取得電腦上正在執行之 Wuapi.dll 的目前檔案版本。</span><span class="sxs-lookup"><span data-stu-id="fc223-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="fc223-111">在 WUA 1.0 中不支援 [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="fc223-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
