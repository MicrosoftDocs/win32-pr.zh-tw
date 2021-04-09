---
title: 安全性應用程式偵測規則更新
description: 安全性應用程式偵測規則更新
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024225"
---
# <a name="security-app-detection-rules-update"></a><span data-ttu-id="8718f-103">安全性應用程式偵測規則更新</span><span class="sxs-lookup"><span data-stu-id="8718f-103">Security app detection rules update</span></span>

## <a name="platforms"></a><span data-ttu-id="8718f-104">平台</span><span class="sxs-lookup"><span data-stu-id="8718f-104">Platforms</span></span>

<span data-ttu-id="8718f-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="8718f-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8718f-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8718f-106">**Servers** – Windows Server 2012</span></span>  


### <a name="description"></a><span data-ttu-id="8718f-107">Description</span><span class="sxs-lookup"><span data-stu-id="8718f-107">Description</span></span>

<span data-ttu-id="8718f-108">在 Windows 8 中新增的 Windows Store 應用程式全部都安裝到 [Program Files] 下的一般位置， (% programfiles% ) 稱為 [ \\ program files \\ WindowsApps]。</span><span class="sxs-lookup"><span data-stu-id="8718f-108">The Windows Store apps being added in Windows 8 are all being installed to a common location under “Program Files” (%programfiles%) called \\program files\\WindowsApps.</span></span>

### <a name="manifestation"></a><span data-ttu-id="8718f-109">表現</span><span class="sxs-lookup"><span data-stu-id="8718f-109">Manifestation</span></span>

<span data-ttu-id="8718f-110">這可能會使現有的設定發生衝突，而某些防毒軟體/反惡意程式碼偵測器會將這個位置視為原因的可能位置。</span><span class="sxs-lookup"><span data-stu-id="8718f-110">This can cause collisions with existing configurations, and some antivirus/anti-malware detectors see this location as a potential location that is a cause for concern.</span></span>

### <a name="mitigation"></a><span data-ttu-id="8718f-111">降低</span><span class="sxs-lookup"><span data-stu-id="8718f-111">Mitigation</span></span>

<span data-ttu-id="8718f-112">目前的建議如下：</span><span class="sxs-lookup"><span data-stu-id="8718f-112">The current recommendations are:</span></span>

-   <span data-ttu-id="8718f-113">移離 [ \\ 程式檔] \\ WindowsApps 以儲存任何自訂應用程式</span><span class="sxs-lookup"><span data-stu-id="8718f-113">Move away from \\program files\\WindowsApps for storing any custom apps</span></span>
-   <span data-ttu-id="8718f-114">防毒軟體廠商應該更新其啟發學習法，使其不會將該位置識別為惡意程式碼位置</span><span class="sxs-lookup"><span data-stu-id="8718f-114">Antivirus/antimalware vendors should update their heuristics so they do not identify that location as a malware location</span></span>

 

 




