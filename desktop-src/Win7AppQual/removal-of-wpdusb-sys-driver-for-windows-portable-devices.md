---
description: 移除 Windows 可攜式裝置的 WPDUSB.SYS 驅動程式
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: 移除 Windows 可攜式裝置的 WPDUSB.SYS 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116246"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="50682-103">移除 Windows 可攜式裝置的 WPDUSB.SYS 驅動程式</span><span class="sxs-lookup"><span data-stu-id="50682-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="50682-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="50682-104">Affected Platforms</span></span>

<span data-ttu-id="50682-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="50682-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="50682-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50682-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="50682-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="50682-107">Feature Impact</span></span>

 <span data-ttu-id="50682-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="50682-108">**Severity** - Low</span></span>  
<span data-ttu-id="50682-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="50682-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="50682-110">Description</span><span class="sxs-lookup"><span data-stu-id="50682-110">Description</span></span>

<span data-ttu-id="50682-111">Microsoft 已將 windows Vista USB 驅動程式堆疊 (WPDUSB.SYS) 的核心模式元件取代為一般 WINUSB.SYS 驅動程式 (WPD) 。</span><span class="sxs-lookup"><span data-stu-id="50682-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="50682-112">與原始 WPDUSB.SYS 驅動程式進行通訊的方式，是透過私用 i/o 控制項 (IOCTL) 程式碼;這些服務的支援也已被移除。</span><span class="sxs-lookup"><span data-stu-id="50682-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="50682-113">這些 IOCTL 程式碼的任何取用者都必須負責適當地解讀和實行媒體傳輸通訊協定， (MTP) 。</span><span class="sxs-lookup"><span data-stu-id="50682-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="50682-114">Windows Vista 不支援協力廠商應用程式使用這些 IOCTL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="50682-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="50682-115">影響的表現</span><span class="sxs-lookup"><span data-stu-id="50682-115">Manifestation of Impact</span></span>

<span data-ttu-id="50682-116">任何相依于這些私用 IOCTL 程式碼可用性的應用程式，都將無法再存取 USB 連接的 MTP 裝置。</span><span class="sxs-lookup"><span data-stu-id="50682-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="50682-117">降低</span><span class="sxs-lookup"><span data-stu-id="50682-117">Mitigation</span></span>

<span data-ttu-id="50682-118">相依于私用 IOCTL 程式碼之應用程式的使用者，必須使用不同的應用程式 (或應用程式的更新版本) 存取 USB 連接的 MTP 裝置。</span><span class="sxs-lookup"><span data-stu-id="50682-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="50682-119">解決方法</span><span class="sxs-lookup"><span data-stu-id="50682-119">Solution</span></span>

<span data-ttu-id="50682-120">應用程式應該使用 Windows 可攜式裝置 (WPD) API 來尋找任何 WPD 裝置並與其互動。</span><span class="sxs-lookup"><span data-stu-id="50682-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="50682-121">雖然 WPD 裝置的大量百分比會實作為與電腦通訊的 MTP，但 WPD 並不只限于 MTP 裝置。</span><span class="sxs-lookup"><span data-stu-id="50682-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="50682-122">此外，透過私用 IOCTLs 直接存取裝置會限制應用程式只能與 USB 連接的裝置進行通訊，使用 WPD API 會將連線選項清單擴充到其他通訊協定 (例如，Wi-fi) 。</span><span class="sxs-lookup"><span data-stu-id="50682-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="50682-123">在罕見的情況下，當應用程式必須是 MTP 感知時，WPD API 會提供原始 MTP 命令的傳遞機制。</span><span class="sxs-lookup"><span data-stu-id="50682-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="50682-124">運用功能功能</span><span class="sxs-lookup"><span data-stu-id="50682-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="50682-125">Windows XP (透過 windows 格式 SDK) 、Windows Vista 和 Windows 7 支援 WPD API。</span><span class="sxs-lookup"><span data-stu-id="50682-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="50682-126">Windows 7 的 WPD 執行透過藍牙新增對 MTP 的支援。</span><span class="sxs-lookup"><span data-stu-id="50682-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="50682-127">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="50682-127">Links to Other Resources</span></span>

[<span data-ttu-id="50682-128">Windows 可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="50682-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
