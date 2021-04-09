---
title: 使用 IMAPI.EXE
description: 下列主題示範如何使用「映射主控 API」。
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840832"
---
# <a name="using-imapi"></a><span data-ttu-id="1f183-103">使用 IMAPI.EXE</span><span class="sxs-lookup"><span data-stu-id="1f183-103">Using IMAPI</span></span>

<span data-ttu-id="1f183-104">下列主題示範如何使用「映射主控 API」。</span><span class="sxs-lookup"><span data-stu-id="1f183-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="1f183-105">使用案例</span><span class="sxs-lookup"><span data-stu-id="1f183-105">Usage Scenarios</span></span>

<span data-ttu-id="1f183-106">下列檔提供常見 IMAPI.EXE 案例的詳細指導方針。</span><span class="sxs-lookup"><span data-stu-id="1f183-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="1f183-107">狀況</span><span class="sxs-lookup"><span data-stu-id="1f183-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="1f183-108">描述</span><span class="sxs-lookup"><span data-stu-id="1f183-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f183-109">檢查磁片磁碟機支援</span><span class="sxs-lookup"><span data-stu-id="1f183-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="1f183-110">示範對媒體磁片磁碟機的支援偵測。</span><span class="sxs-lookup"><span data-stu-id="1f183-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="1f183-111">檢查媒體支援</span><span class="sxs-lookup"><span data-stu-id="1f183-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="1f183-112">示範對媒體支援的偵測。</span><span class="sxs-lookup"><span data-stu-id="1f183-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="1f183-113">燒錄光碟影像</span><span class="sxs-lookup"><span data-stu-id="1f183-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="1f183-114">示範如何使用 IMAPI.EXE) 燒錄光碟 (燒錄光碟。</span><span class="sxs-lookup"><span data-stu-id="1f183-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="1f183-115">新增開機映射</span><span class="sxs-lookup"><span data-stu-id="1f183-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="1f183-116">藉由新增程式碼以在光碟的開機區段中包含可開機映射，以 [燒錄光碟映射](burning-a-disc.md) 範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="1f183-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="1f183-117">建立多會話光碟</span><span class="sxs-lookup"><span data-stu-id="1f183-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="1f183-118">示範如何使用 IMAPI.EXE 建立多會話光碟。</span><span class="sxs-lookup"><span data-stu-id="1f183-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="1f183-119">監視事件的進度</span><span class="sxs-lookup"><span data-stu-id="1f183-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="1f183-120">示範如何使用特定介面，以允許事件處理常式的執行，以便接收進度資訊。</span><span class="sxs-lookup"><span data-stu-id="1f183-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="1f183-121">在燒錄期間防止登出或暫停</span><span class="sxs-lookup"><span data-stu-id="1f183-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="1f183-122">包含詳細說明在 Windows 中涉及使用者「登出」和「暫停」之案例的應用程式開發考慮。</span><span class="sxs-lookup"><span data-stu-id="1f183-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="1f183-123">提供媒體燒錄裝置的使用者權限</span><span class="sxs-lookup"><span data-stu-id="1f183-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="1f183-124">詳細說明在 Windows XP 及 Windows Server 2003 上，確保使用者有足夠的許可權可使用媒體燒錄裝置所需的程式。</span><span class="sxs-lookup"><span data-stu-id="1f183-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="1f183-125">應用程式相容性</span><span class="sxs-lookup"><span data-stu-id="1f183-125">Application Compatibility</span></span>

<span data-ttu-id="1f183-126">下列檔包含開發使用 IMAPI.EXE 的應用程式時所需考慮的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="1f183-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="1f183-127">指引</span><span class="sxs-lookup"><span data-stu-id="1f183-127">Guidance</span></span>                                                   | <span data-ttu-id="1f183-128">描述</span><span class="sxs-lookup"><span data-stu-id="1f183-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f183-129">IMAPI.EXE 多會話配置</span><span class="sxs-lookup"><span data-stu-id="1f183-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="1f183-130">詳細說明 IMAPI.EXE 利用來執行多會話的光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="1f183-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="1f183-131">這項資訊是用來確保 IMAPI.EXE 與其他燒錄軟體之間的互通性，並允許建立 IMAPI.EXE 相容的多會話光碟映射。</span><span class="sxs-lookup"><span data-stu-id="1f183-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





