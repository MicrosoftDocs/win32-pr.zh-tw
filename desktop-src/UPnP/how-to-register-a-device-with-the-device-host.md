---
title: 如何向裝置主機註冊裝置
description: 您可以註冊正在執行的裝置或非執行中的裝置。
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021487"
---
# <a name="how-to-register-a-device-with-the-device-host"></a><span data-ttu-id="e3665-103">如何向裝置主機註冊裝置</span><span class="sxs-lookup"><span data-stu-id="e3665-103">How to Register a Device with the Device Host</span></span>

<span data-ttu-id="e3665-104">您可以註冊正在執行的裝置或非執行中的裝置。</span><span class="sxs-lookup"><span data-stu-id="e3665-104">You can register either a running device or a non-running device.</span></span>

## <a name="registering-a-running-device"></a><span data-ttu-id="e3665-105">註冊正在執行的裝置</span><span class="sxs-lookup"><span data-stu-id="e3665-105">Registering a Running Device</span></span>

<span data-ttu-id="e3665-106">裝置是使用 [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) 介面註冊的。</span><span class="sxs-lookup"><span data-stu-id="e3665-106">Devices are registered using the [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) interface.</span></span> <span data-ttu-id="e3665-107">只有系統管理員才可以註冊執行中的裝置。</span><span class="sxs-lookup"><span data-stu-id="e3665-107">Only administrators are allowed to register running devices.</span></span> <span data-ttu-id="e3665-108">若要註冊具有正在執行之裝置控制物件的裝置，應用程式必須叫用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)，並傳遞下列各項：</span><span class="sxs-lookup"><span data-stu-id="e3665-108">To register a device that has a running device control object, an application must invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passing the following:</span></span>

-   <span data-ttu-id="e3665-109">裝置描述的文字。</span><span class="sxs-lookup"><span data-stu-id="e3665-109">The text of the device's description.</span></span>
-   <span data-ttu-id="e3665-110">裝置控制物件的 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="e3665-110">An **IUnknown** pointer to the device control object.</span></span>
-   <span data-ttu-id="e3665-111">傳遞至裝置控制項物件之 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法的初始化字串。</span><span class="sxs-lookup"><span data-stu-id="e3665-111">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="e3665-112">資原始目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="e3665-112">The location of the resource directory.</span></span>
-   <span data-ttu-id="e3665-113">裝置的存留期。</span><span class="sxs-lookup"><span data-stu-id="e3665-113">The lifetime of the device.</span></span>
-   <span data-ttu-id="e3665-114">裝置識別碼參數 (OUT 參數) ，也就是此呼叫的傳回值;在 c + + 中會傳回裝置識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="e3665-114">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

## <a name="registering-a-non-running-device"></a><span data-ttu-id="e3665-115">註冊非執行中的裝置</span><span class="sxs-lookup"><span data-stu-id="e3665-115">Registering a Non-Running Device</span></span>

<span data-ttu-id="e3665-116">依預設，只允許系統管理員和互動式使用者註冊非執行中的裝置。</span><span class="sxs-lookup"><span data-stu-id="e3665-116">By default, only administrators and interactive users are allowed to register non-running devices.</span></span> <span data-ttu-id="e3665-117">若要向未執行的裝置控制項物件註冊裝置，應用程式會使用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) 方法。</span><span class="sxs-lookup"><span data-stu-id="e3665-117">To register a device with a device control object that is not running, the application uses the [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) method.</span></span>

<span data-ttu-id="e3665-118">若要以程式設計方式向未執行的裝置控制物件註冊裝置，應用程式必須叫用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) ，並將下列參數傳遞給它：</span><span class="sxs-lookup"><span data-stu-id="e3665-118">To programmatically register a device with a non-running device control object, the application must invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) and pass it the following parameters:</span></span>

-   <span data-ttu-id="e3665-119">裝置描述的文字。</span><span class="sxs-lookup"><span data-stu-id="e3665-119">The text of the device's description.</span></span>
-   <span data-ttu-id="e3665-120">裝置控制物件的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="e3665-120">The ProgID of the device control object.</span></span>
-   <span data-ttu-id="e3665-121">傳遞至裝置控制項物件之 [**IUPnPDeviceControl：： Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) 方法的初始化字串。</span><span class="sxs-lookup"><span data-stu-id="e3665-121">An initialization string that is passed to the device control object's [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) method.</span></span>
-   <span data-ttu-id="e3665-122">容器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3665-122">A container ID.</span></span>
-   <span data-ttu-id="e3665-123">資原始目錄的位置。</span><span class="sxs-lookup"><span data-stu-id="e3665-123">The location of the resource directory.</span></span>
-   <span data-ttu-id="e3665-124">裝置的存留期。</span><span class="sxs-lookup"><span data-stu-id="e3665-124">The lifetime of the device.</span></span>
-   <span data-ttu-id="e3665-125">裝置識別碼參數 (OUT 參數) ，也就是此呼叫的傳回值;在 c + + 中會傳回裝置識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="e3665-125">The Device ID parameter (an OUT parameter), which is the return value of this call; a pointer to the Device ID is returned in C++.</span></span>

<span data-ttu-id="e3665-126">未執行裝置的註冊可設定為跨系統開機， (在關閉階段) 期間未發佈裝置。</span><span class="sxs-lookup"><span data-stu-id="e3665-126">The registrations of non-running devices can be configured to persist across system boots (the devices are unpublished during the shutdown phase).</span></span> <span data-ttu-id="e3665-127">因此，如果以這種方式設定，則會在每次電腦開機時發佈並宣告裝置。</span><span class="sxs-lookup"><span data-stu-id="e3665-127">Therefore, if they are configured this way, devices are published and announced every time the computer is booted.</span></span>

 

 




