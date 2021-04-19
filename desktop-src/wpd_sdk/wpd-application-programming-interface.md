---
description: WPD 應用程式設計介面
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: WPD 應用程式設計介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975233"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="0c66c-103">WPD 應用程式設計介面</span><span class="sxs-lookup"><span data-stu-id="0c66c-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="0c66c-104">在 Windows 可攜式裝置上建立的應用程式可以探索裝置、傳送和接收內容，甚至控制裝置，例如拍攝圖片或傳送文字訊息。</span><span class="sxs-lookup"><span data-stu-id="0c66c-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="0c66c-105">系統設計為具有彈性，因此可以探索許多類型的裝置，並可進行擴充，讓驅動程式開發人員可以定義自訂裝置的自訂屬性和命令。</span><span class="sxs-lookup"><span data-stu-id="0c66c-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="0c66c-106">下表描述此檔的主要主題。</span><span class="sxs-lookup"><span data-stu-id="0c66c-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="0c66c-107">主題</span><span class="sxs-lookup"><span data-stu-id="0c66c-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="0c66c-108">描述</span><span class="sxs-lookup"><span data-stu-id="0c66c-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c66c-109">應用程式開發的一般需求</span><span class="sxs-lookup"><span data-stu-id="0c66c-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="0c66c-110">使用 Windows 可攜式裝置開發驅動程式和應用程式的硬體和軟體需求。</span><span class="sxs-lookup"><span data-stu-id="0c66c-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="0c66c-111">Windows Media DRM-Enabled 應用程式的需求</span><span class="sxs-lookup"><span data-stu-id="0c66c-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="0c66c-112">啟用 Windows Media 受 DRM 保護的內容傳輸所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="0c66c-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="0c66c-113">範例</span><span class="sxs-lookup"><span data-stu-id="0c66c-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="0c66c-114">此軟體發展工具組所提供的兩個命令列桌面應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="0c66c-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="0c66c-115">應用程式總覽</span><span class="sxs-lookup"><span data-stu-id="0c66c-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="0c66c-116">Windows 可攜式裝置中使用的重要概念。</span><span class="sxs-lookup"><span data-stu-id="0c66c-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="0c66c-117">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="0c66c-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="0c66c-118">應用程式將執行的主要工作，以及逐步指示和程式碼片段。</span><span class="sxs-lookup"><span data-stu-id="0c66c-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="0c66c-119">程式設計參考</span><span class="sxs-lookup"><span data-stu-id="0c66c-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="0c66c-120">Windows 可攜式裝置所定義之介面和資料類型的參考指南。</span><span class="sxs-lookup"><span data-stu-id="0c66c-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="0c66c-121">以 Windows Media 裝置管理員或 Windows 映像取得建立的應用程式可以透過相容性層存取 Windows 可攜式裝置。</span><span class="sxs-lookup"><span data-stu-id="0c66c-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="0c66c-122">Microsoft 提供數個標準通訊協定和裝置的驅動程式，包括媒體傳輸通訊協定 (MTP) 裝置和大型儲存類別 (SERVICES.MSC) 裝置。</span><span class="sxs-lookup"><span data-stu-id="0c66c-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="0c66c-123">如果您熟悉 User-Mode 驅動程式架構，您可以為自訂裝置開發自己的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0c66c-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



