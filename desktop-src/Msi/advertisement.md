---
description: Windows Installer 可以將應用程式的可用性通告給使用者或其他應用程式，而無須實際安裝應用程式。
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: 廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999882"
---
# <a name="advertisement"></a><span data-ttu-id="ac138-103">廣告</span><span class="sxs-lookup"><span data-stu-id="ac138-103">Advertisement</span></span>

<span data-ttu-id="ac138-104">Windows Installer 可以將應用程式的可用性通告給使用者或其他應用程式，而無須實際安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac138-104">The Windows Installer can advertise the availability of an application to users or other applications without actually installing the application.</span></span> <span data-ttu-id="ac138-105">如果已公告應用程式，則只會對使用者或其他應用程式顯示載入和啟動應用程式所需的介面。</span><span class="sxs-lookup"><span data-stu-id="ac138-105">If an application is advertised, only the interfaces required for loading and launching the application are presented to the user or other applications.</span></span> <span data-ttu-id="ac138-106">如果使用者或應用程式啟動已公告的介面，安裝程式就會繼續安裝所需的元件，如 [隨選安裝](installation-on-demand.md)所述。</span><span class="sxs-lookup"><span data-stu-id="ac138-106">If a user or application activates an advertised interface the installer then proceeds to install the necessary components as described in [Installation-On-Demand](installation-on-demand.md).</span></span>

<span data-ttu-id="ac138-107">這兩種類型的廣告是指派和發佈的。</span><span class="sxs-lookup"><span data-stu-id="ac138-107">The two types of advertising are assigning and publishing.</span></span> <span data-ttu-id="ac138-108">當應用程式指派給使用者時，應用程式就會顯示安裝給使用者。</span><span class="sxs-lookup"><span data-stu-id="ac138-108">An application appears installed to a user when that application is assigned to the user.</span></span> <span data-ttu-id="ac138-109">[ **開始** ] 功能表包含適當的快捷方式、顯示圖示、檔案與應用程式相關聯，以及登錄專案會反映應用程式的安裝。</span><span class="sxs-lookup"><span data-stu-id="ac138-109">The **Start** menu contains the appropriate shortcuts, icons are displayed, files are associated with the application, and registry entries reflect the application's installation.</span></span> <span data-ttu-id="ac138-110">當使用者嘗試開啟指派的應用程式時，它會隨選安裝。</span><span class="sxs-lookup"><span data-stu-id="ac138-110">When the user tries to open an assigned application it is installed upon demand.</span></span>

<span data-ttu-id="ac138-111">安裝程式會根據作業系統支援應用程式和功能的公告。</span><span class="sxs-lookup"><span data-stu-id="ac138-111">The installer supports the advertisement of applications and features according to the operating system.</span></span> <span data-ttu-id="ac138-112">安裝程式會從 Windows XP 開始，為指派的應用程式註冊 COM 類別資訊。</span><span class="sxs-lookup"><span data-stu-id="ac138-112">The installer registers COM class information for assigned applications beginning with Windows XP.</span></span> <span data-ttu-id="ac138-113">這可讓安裝程式在建立已公告類別的實例時，安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac138-113">This enables the installer to install the application upon the creation of an instance of an advertised class.</span></span> <span data-ttu-id="ac138-114">如需詳細資訊，請參閱 [廣告的平臺支援](platform-support-of-advertisement.md)。</span><span class="sxs-lookup"><span data-stu-id="ac138-114">For more information, see [Platform Support of Advertisement](platform-support-of-advertisement.md).</span></span>

<span data-ttu-id="ac138-115">您可以從 Windows Server 2003 開始的伺服器發行應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac138-115">You can publish an application from the server beginning with Windows Server 2003.</span></span> <span data-ttu-id="ac138-116">然後，已發佈的應用程式會透過其檔案關聯或多用途網際網路郵件延伸模組 (MIME) 類型進行安裝。</span><span class="sxs-lookup"><span data-stu-id="ac138-116">The published application is then installed through its file association or Multipurpose Internet Mail Extension (MIME) type.</span></span> <span data-ttu-id="ac138-117">發佈時，不會在使用者介面中填入任何應用程式的圖示。</span><span class="sxs-lookup"><span data-stu-id="ac138-117">Publishing does not populate the user interface with any of the application's icons.</span></span> <span data-ttu-id="ac138-118">用戶端作業系統可以從 Windows XP 開始安裝已發佈的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ac138-118">The client operating system can install a published application beginning with Windows XP.</span></span>

 

 



