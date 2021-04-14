---
title: 如何使用裝置存取 API
description: 本主題包含使用裝置存取 API 的工作和設計考慮。
ms.assetid: 8D951EB5-4AFB-4051-8F1F-30F847F1A757
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 29c4812c559b691a896fb5bb9da39064bf3c8614
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383194"
---
# <a name="how-to-use-the-device-access-api"></a><span data-ttu-id="97f91-103">如何使用裝置存取 API</span><span class="sxs-lookup"><span data-stu-id="97f91-103">How to Use the Device Access API</span></span>

<span data-ttu-id="97f91-104">本主題包含使用裝置存取 API 的工作和設計考慮。</span><span class="sxs-lookup"><span data-stu-id="97f91-104">This topic contains tasks and design considerations for using the Device Access API.</span></span>

## <a name="steps"></a><span data-ttu-id="97f91-105">步驟</span><span class="sxs-lookup"><span data-stu-id="97f91-105">Steps</span></span>

| <span data-ttu-id="97f91-106">主題</span><span class="sxs-lookup"><span data-stu-id="97f91-106">Topic</span></span> | <span data-ttu-id="97f91-107">描述</span><span class="sxs-lookup"><span data-stu-id="97f91-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="97f91-108">自訂裝置的設計考慮</span><span class="sxs-lookup"><span data-stu-id="97f91-108">Design Considerations for Custom Devices</span></span>](design.md)<br/> | <span data-ttu-id="97f91-109">本主題說明可協助您判斷裝置是否需要自訂驅動程式的設計考慮。</span><span class="sxs-lookup"><span data-stu-id="97f91-109">This topic describes design considerations that can help you determine whether your device needs a custom driver.</span></span><br/> |
| [<span data-ttu-id="97f91-110">執行裝置存取物件</span><span class="sxs-lookup"><span data-stu-id="97f91-110">Implement the Device Access Object</span></span>](create-the-device-access-object.md)<br/> | <span data-ttu-id="97f91-111">本主題說明如何將裝置存取物件具現化，並使用它來存取裝置。</span><span class="sxs-lookup"><span data-stu-id="97f91-111">This topic explains how to instantiate the device access object and use it to access a device.</span></span> <br/>  |
| [<span data-ttu-id="97f91-112">宣告裝置功能</span><span class="sxs-lookup"><span data-stu-id="97f91-112">Declaring the Device Capability</span></span>](declaring-the-device-capability.md)<br/> | <span data-ttu-id="97f91-113">本主題說明如何宣告裝置功能 GUID。</span><span class="sxs-lookup"><span data-stu-id="97f91-113">This topic explains how to declare the device capability GUID.</span></span><br/> |
| [<span data-ttu-id="97f91-114">將裝置介面註冊為受特殊許可權的應用程式限制</span><span class="sxs-lookup"><span data-stu-id="97f91-114">Register the device interface as restricted to privileged apps</span></span>](register-the-device-interface-class-as-privileged.md)<br/> | <span data-ttu-id="97f91-115">本主題說明如何新增 **受限制** 的屬性，指出只有特殊許可權的應用程式可以存取裝置介面類別別。</span><span class="sxs-lookup"><span data-stu-id="97f91-115">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span><br/> |
| [<span data-ttu-id="97f91-116">建立 Windows 執行階段擴充功能</span><span class="sxs-lookup"><span data-stu-id="97f91-116">Create a Windows Runtime Extension</span></span>](create-a-windows-runtime-extension.md)<br/> | <span data-ttu-id="97f91-117">您可以建立 Windows 執行階段元件包裝存取您驅動程式的元件。</span><span class="sxs-lookup"><span data-stu-id="97f91-117">You can create a Windows Runtime component to wrap the component that accesses your driver.</span></span> <span data-ttu-id="97f91-118">然後，您可以使用 c # 或 JavaScript 撰寫裝置的 Windows Store 裝置應用程式。</span><span class="sxs-lookup"><span data-stu-id="97f91-118">You can then write a Windows Store device app for your device in C# or JavaScript.</span></span><br/> |

## <a name="additional-resources"></a><span data-ttu-id="97f91-119">其他資源</span><span class="sxs-lookup"><span data-stu-id="97f91-119">Additional resources</span></span>

- <span data-ttu-id="97f91-120">[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)示範如何使用裝置存取 api，從 Windows Store 裝置應用程式存取自訂驅動程式。</span><span class="sxs-lookup"><span data-stu-id="97f91-120">The [Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) demonstrates how to use the Device Access APIs to access a custom driver from a Windows Store device app.</span></span>
- <span data-ttu-id="97f91-121">[適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) 會提供資源，以深入瞭解如何設計和開發專門裝置的 Windows Store 裝置應用程式。</span><span class="sxs-lookup"><span data-stu-id="97f91-121">[UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) provides resources for learning more about how to design and develop Windows Store device apps for specialized devices.</span></span>
- <span data-ttu-id="97f91-122">[硬體開發人員中心](/windows-hardware/drivers/)提供所有裝置類型通用的 Windows Store 裝置應用程式開發工作的一般資源。</span><span class="sxs-lookup"><span data-stu-id="97f91-122">The [Hardware Dev Center](/windows-hardware/drivers/) provides general resources for Windows Store device app development tasks that are common to all types of devices.</span></span>
