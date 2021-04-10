---
title: 管理藍牙裝置和服務
description: 有兩種主要的藍牙程式設計方法，可讓您使用 Windows 通訊端介面進行 Windows 程式設計，以及直接使用 nonsocket 藍牙介面管理裝置。
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- 管理藍牙裝置和服務
- 藍牙裝置和服務，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092760"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="61f57-105">管理藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="61f57-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="61f57-106">本節說明如何使用藍牙 API 來直接控制藍牙裝置和服務。</span><span class="sxs-lookup"><span data-stu-id="61f57-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="61f57-107">如需有關使用 Windows 通訊端介面在 Windows 上設計藍牙程式的詳細資訊，請參閱 [適用于藍牙的 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。</span><span class="sxs-lookup"><span data-stu-id="61f57-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="61f57-108">藍牙無法防止電源管理功能中斷藍牙傳輸。</span><span class="sxs-lookup"><span data-stu-id="61f57-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="61f57-109">啟用 Bluetooth 的應用程式可以監視電源訊息，以防止這類中斷。</span><span class="sxs-lookup"><span data-stu-id="61f57-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="61f57-110">如需詳細資訊，請參閱 [使用電源管理](/windows/desktop/Power/using-power-management)。</span><span class="sxs-lookup"><span data-stu-id="61f57-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="61f57-111">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="61f57-111">This section contains the following topics.</span></span>

| <span data-ttu-id="61f57-112">區段</span><span class="sxs-lookup"><span data-stu-id="61f57-112">Section</span></span>                                                                               | <span data-ttu-id="61f57-113">Content</span><span class="sxs-lookup"><span data-stu-id="61f57-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="61f57-114">選取藍牙裝置</span><span class="sxs-lookup"><span data-stu-id="61f57-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="61f57-115">說明如何選取藍牙裝置。</span><span class="sxs-lookup"><span data-stu-id="61f57-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="61f57-116">藍牙和 WM \_ DEVICECHANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="61f57-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="61f57-117">說明藍牙與 **WM \_ DEVICECHANGE** 訊息之間的互動。</span><span class="sxs-lookup"><span data-stu-id="61f57-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 