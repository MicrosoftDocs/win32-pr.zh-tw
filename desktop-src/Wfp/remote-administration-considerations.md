---
description: 遠端系統管理的系統有一些獨特的考慮。
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: WFP 遠端系統管理考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997867"
---
# <a name="wfp-remote-administration-considerations"></a><span data-ttu-id="2a7d3-103">WFP 遠端系統管理考慮</span><span class="sxs-lookup"><span data-stu-id="2a7d3-103">WFP Remote Administration Considerations</span></span>

<span data-ttu-id="2a7d3-104">遠端系統管理的系統有一些獨特的考慮。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-104">There are some considerations that are unique to remotely administered systems.</span></span> <span data-ttu-id="2a7d3-105">首先，當軟體安裝是使用 SMS 或 MSI) 從遠端部署 (時，[WFP 錯誤] 對話方塊會顯示在本機登入的系統管理員 (（如果有) 的話），而不是安裝服務的螢幕上。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-105">First, when software installation is remotely deployed (using SMS or MSI), WFP error dialog boxes are displayed on the screen of a locally logged on administrator (if present), not to the installation service.</span></span> <span data-ttu-id="2a7d3-106">其次，如果系統管理員從遠端登入到終端機伺服器，並安裝取代受保護系統檔案的應用程式，則 [WFP 錯誤] 對話方塊只會顯示在主主控台，而不會顯示在系統管理員的遠端視窗中。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-106">Second, if an administrator logs into a terminal server remotely and installs an application that replaces protected system files, the WFP error dialog boxes are displayed only in the main console, not the administrator's remote window.</span></span>

<span data-ttu-id="2a7d3-107">基於這些理由，WFP 會隱藏其錯誤對話方塊，直到系統管理員在本機登入。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-107">For these reasons, WFP suppresses its error dialog boxes until an administrator logs on locally.</span></span> <span data-ttu-id="2a7d3-108">遠端系統管理員可以在系統事件記錄檔中找到檔案取代錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-108">Remote administrators can find file replacement errors in the system event log.</span></span>

<span data-ttu-id="2a7d3-109">**Windows Vista 和 Windows Server 2008：** 不支援 WFP 遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="2a7d3-109">**Windows Vista and Windows Server 2008:** WFP remote administration is not supported.</span></span>

 

 



