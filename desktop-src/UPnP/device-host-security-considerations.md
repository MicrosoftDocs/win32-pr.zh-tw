---
title: 裝置主機安全性考慮
description: 使用裝置主機會產生安全性問題。
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463288"
---
# <a name="device-host-security-considerations"></a><span data-ttu-id="fe895-103">裝置主機安全性考慮</span><span class="sxs-lookup"><span data-stu-id="fe895-103">Device Host Security Considerations</span></span>

<span data-ttu-id="fe895-104">使用裝置主機會因為下列原因而產生安全性問題：</span><span class="sxs-lookup"><span data-stu-id="fe895-104">Using the device host creates security issues because of the following:</span></span>

-   <span data-ttu-id="fe895-105">在執行 Windows XP 的電腦上主控的裝置會在所有網路上傳送公告。</span><span class="sxs-lookup"><span data-stu-id="fe895-105">Devices hosted on a computer running Windows XP sends announcements on all networks.</span></span>
-   <span data-ttu-id="fe895-106">在執行 Windows XP 的電腦上主控的裝置，可讓您控制來自所有網路的裝置。</span><span class="sxs-lookup"><span data-stu-id="fe895-106">Devices hosted on a computer running Windows XP allow control of devices from all networks.</span></span>

<span data-ttu-id="fe895-107">這會增加家用取用者的風險，因為在執行 Windows XP 的電腦上，像是媒體播放機或橋接光源或 HVAC 系統等裝置都可以看見，而且可以從家裡以外的控制點控制。</span><span class="sxs-lookup"><span data-stu-id="fe895-107">This increases the risk to home consumers, because devices such as a media player or a bridged lighting or HVAC system hosted on a computer running Windows XP are visible and can be controlled from control points outside the home.</span></span>

<span data-ttu-id="fe895-108">當您建立託管裝置時，您必須考慮一些安全性問題。</span><span class="sxs-lookup"><span data-stu-id="fe895-108">When you are creating a hosted device, you need to take into consideration some security issues.</span></span>

-   <span data-ttu-id="fe895-109">為了減少探索和攻擊 UPnP 型裝置的範圍，所有 SSDP 訊息的 TTL 都是1。</span><span class="sxs-lookup"><span data-stu-id="fe895-109">To reduce the scope of discovery and attack of UPnP-based devices, the TTL of all SSDP messages is 1.</span></span> <span data-ttu-id="fe895-110">這表示已註冊的裝置只會由相同網路上的控制點來探索。</span><span class="sxs-lookup"><span data-stu-id="fe895-110">This means that a registered device is only discovered by control points on the same network.</span></span> <span data-ttu-id="fe895-111">您可以在登錄中設定較高的 TTL。</span><span class="sxs-lookup"><span data-stu-id="fe895-111">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="fe895-112">註冊非執行中的裝置需要預先註冊具有 COM 的 device .dll，這需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="fe895-112">Registering a non-running device requires pre-registering the device .dll with COM, which requires administrator privilege.</span></span>
-   <span data-ttu-id="fe895-113">註冊正在執行的裝置需要系統管理員、本機服務或本機系統許可權。</span><span class="sxs-lookup"><span data-stu-id="fe895-113">Registering a running device requires Administrator, Local Service, or Local System privilege.</span></span>
-   <span data-ttu-id="fe895-114">當裝置主機啟動時，它會以 [LocalService](/windows/desktop/Services/localservice-account)的形式執行。</span><span class="sxs-lookup"><span data-stu-id="fe895-114">When the device host is started, it is run as [LocalService](/windows/desktop/Services/localservice-account).</span></span> <span data-ttu-id="fe895-115">這讓裝置能夠產生審核和讀取 **HKEY \_ 本機 \_ 電腦** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="fe895-115">This gives the device the ability to generate audits and read the **HKEY\_LOCAL\_MACHINE** registry key.</span></span> <span data-ttu-id="fe895-116">裝置可以存取 **HKEY \_ 目前的 \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="fe895-116">The device does have access to **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="fe895-117">LocalService 帳戶可以使用已授與 LocalService 存取權的資源，以及授與存取權給 AuthenticatedUser 的資源。</span><span class="sxs-lookup"><span data-stu-id="fe895-117">The LocalService account can use resources to which LocalService has been granted access, as well as those that grant access to AuthenticatedUser.</span></span> <span data-ttu-id="fe895-118">裝置具有受限的檔案系統存取權。</span><span class="sxs-lookup"><span data-stu-id="fe895-118">The device has restricted file system access.</span></span>
-   <span data-ttu-id="fe895-119">必須更新檔案系統 Acl，以允許 [LocalService](/windows/desktop/Services/localservice-account) 存取資原始目錄。</span><span class="sxs-lookup"><span data-stu-id="fe895-119">The file system ACLs must be updated to allow [LocalService](/windows/desktop/Services/localservice-account) access to the resource directory.</span></span>
-   <span data-ttu-id="fe895-120">如果您的裝置必須有更多的安全性存取權，您可以為裝置建立自己的進程，並使用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)來註冊它。</span><span class="sxs-lookup"><span data-stu-id="fe895-120">If your device must have more security access, you can create your own process for the device and register it by using [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).</span></span>

 

 