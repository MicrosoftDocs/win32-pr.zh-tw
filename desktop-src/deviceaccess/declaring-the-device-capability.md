---
title: 宣告裝置功能
description: 本主題說明如何宣告裝置功能 GUID。
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103933700"
---
# <a name="declaring-the-device-capability"></a><span data-ttu-id="4c4f0-103">宣告裝置功能</span><span class="sxs-lookup"><span data-stu-id="4c4f0-103">Declaring the Device Capability</span></span>

<span data-ttu-id="4c4f0-104">本主題說明如何宣告裝置功能 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c4f0-104">This topic explains how to declare the device capability GUID.</span></span> <span data-ttu-id="4c4f0-105">所有以自訂驅動程式為目標的應用程式都必須宣告這項功能。</span><span class="sxs-lookup"><span data-stu-id="4c4f0-105">All applications that target custom drivers must declare this capability.</span></span>

<span data-ttu-id="4c4f0-106">在您的應用程式資訊清單中，您必須新增裝置功能，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4c4f0-106">In your application manifest, you'll need to add a device capability, as follows:</span></span>

<span data-ttu-id="4c4f0-107">這是自訂裝置的功能聲明範例。</span><span class="sxs-lookup"><span data-stu-id="4c4f0-107">This is an example of a capability declaration for a custom device.</span></span> <span data-ttu-id="4c4f0-108">GUID 是裝置介面類別別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="4c4f0-108">The GUID is the GUID of the device interface class.</span></span>

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a><span data-ttu-id="4c4f0-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c4f0-109">Related topics</span></span>

<span data-ttu-id="4c4f0-110">[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="4c4f0-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
