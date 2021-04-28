---
description: 移除 Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: 移除 Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116266"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="390c0-103">移除 Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="390c0-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="390c0-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="390c0-104">Affected Platforms</span></span>

<span data-ttu-id="390c0-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="390c0-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="390c0-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="390c0-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="390c0-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="390c0-107">Feature Impact</span></span>

 <span data-ttu-id="390c0-108">**嚴重性** -高</span><span class="sxs-lookup"><span data-stu-id="390c0-108">**Severity** - High</span></span>  
<span data-ttu-id="390c0-109">**頻率** -中型</span><span class="sxs-lookup"><span data-stu-id="390c0-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="390c0-110">Description</span><span class="sxs-lookup"><span data-stu-id="390c0-110">Description</span></span>

<span data-ttu-id="390c0-111">Microsoft 淘汰和移除 Windows Movie Maker 公用程式。</span><span class="sxs-lookup"><span data-stu-id="390c0-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="390c0-112">這包括：</span><span class="sxs-lookup"><span data-stu-id="390c0-112">This includes:</span></span>

-   <span data-ttu-id="390c0-113">Windows Movie Maker 的所有進入點 (例如，[開始] 功能表、[開始] > 執行) </span><span class="sxs-lookup"><span data-stu-id="390c0-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="390c0-114">Windows Movie Maker 所使用的所有二進位檔 (% ProgramFiles% Movie Maker 中的所有內容 \\) </span><span class="sxs-lookup"><span data-stu-id="390c0-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="390c0-115">但是，使用者的 Movie Maker 專案檔會保留在系統上，並可供其他支援此檔案格式的應用程式存取。</span><span class="sxs-lookup"><span data-stu-id="390c0-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="390c0-116">表現</span><span class="sxs-lookup"><span data-stu-id="390c0-116">Manifestation</span></span>

<span data-ttu-id="390c0-117">移除 Windows Movie Maker 會導致下列情況：</span><span class="sxs-lookup"><span data-stu-id="390c0-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="390c0-118">任何使用命令列引數啟動 Windows Movie Maker 的嘗試都會失敗</span><span class="sxs-lookup"><span data-stu-id="390c0-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="390c0-119">已安裝以啟用新轉換和動畫的任何外掛程式都會保持安裝，但不會向使用者公開</span><span class="sxs-lookup"><span data-stu-id="390c0-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="390c0-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="390c0-120">Solution</span></span>

<span data-ttu-id="390c0-121">若要在未來擁有這類功能，使用者將需要安裝 Microsoft 或其他軟體提供者的類似應用程式。</span><span class="sxs-lookup"><span data-stu-id="390c0-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



