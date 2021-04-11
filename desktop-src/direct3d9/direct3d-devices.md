---
description: Direct3D 裝置是 Direct3D 的轉譯元件。 它會封裝和儲存呈現狀態。 此外，Direct3D 裝置會執行轉換和燈光作業，並將影像柵格化至介面。
ms.assetid: b592edb8-351a-4a82-9ff7-8a69d82723bc
title: 'Direct3d 裝置 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07726069b952ba99d608e5f36df8e1fb7745cd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187464"
---
# <a name="direct3d-devices-direct3d-9"></a><span data-ttu-id="0af0e-105">Direct3d 裝置 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="0af0e-105">Direct3D Devices (Direct3D 9)</span></span>

<span data-ttu-id="0af0e-106">Direct3D 裝置是 Direct3D 的轉譯元件。</span><span class="sxs-lookup"><span data-stu-id="0af0e-106">A Direct3D device is the rendering component of Direct3D.</span></span> <span data-ttu-id="0af0e-107">它會封裝和儲存呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="0af0e-107">It encapsulates and stores the rendering state.</span></span> <span data-ttu-id="0af0e-108">此外，Direct3D 裝置會執行轉換和燈光作業，並將影像柵格化至介面。</span><span class="sxs-lookup"><span data-stu-id="0af0e-108">In addition, a Direct3D device performs transformations and lighting operations and rasterizes an image to a surface.</span></span>

-   [<span data-ttu-id="0af0e-109">XPDM 和 WDDM</span><span class="sxs-lookup"><span data-stu-id="0af0e-109">XPDM vs. WDDM</span></span>](xpdm-vs-wddm.md)
-   [<span data-ttu-id="0af0e-110"> (Direct3D 9) 的裝置類型 </span><span class="sxs-lookup"><span data-stu-id="0af0e-110">Device Types (Direct3D 9)</span></span>](device-types.md)
-   [<span data-ttu-id="0af0e-111"> (Direct3D 9) 建立裝置 </span><span class="sxs-lookup"><span data-stu-id="0af0e-111">Creating a Device (Direct3D 9)</span></span>](creating-a-device.md)
-   [<span data-ttu-id="0af0e-112"> (Direct3D 9) 的視窗型 vs Full-Screen 模式 </span><span class="sxs-lookup"><span data-stu-id="0af0e-112">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>](windowed-vs-full-screen-mode.md)
-   [<span data-ttu-id="0af0e-113">選取 (Direct3D 9) 的裝置 </span><span class="sxs-lookup"><span data-stu-id="0af0e-113">Selecting a Device (Direct3D 9)</span></span>](selecting-a-device.md)
-   [<span data-ttu-id="0af0e-114"> (Direct3D 9) 的裝置遺失 </span><span class="sxs-lookup"><span data-stu-id="0af0e-114">Lost Devices (Direct3D 9)</span></span>](lost-devices.md)
-   [<span data-ttu-id="0af0e-115">判斷 (Direct3D 9) 的硬體支援 </span><span class="sxs-lookup"><span data-stu-id="0af0e-115">Determining Hardware Support (Direct3D 9)</span></span>](determining-hardware-support.md)
-   [<span data-ttu-id="0af0e-116">處理 (Direct3D 9) 的頂點資料 </span><span class="sxs-lookup"><span data-stu-id="0af0e-116">Processing Vertex Data (Direct3D 9)</span></span>](processing-vertex-data.md)
-   [<span data-ttu-id="0af0e-117">基本</span><span class="sxs-lookup"><span data-stu-id="0af0e-117">Primitives</span></span>](primitives.md)

<span data-ttu-id="0af0e-118">架構上來說，Direct3D 裝置包含轉換模組、光源模組及點陣化模組，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="0af0e-118">Architecturally, Direct3D devices contain a transformation module, a lighting module, and a rasterizing module, as the following diagram shows.</span></span>

![Direct3D 裝置架構圖](images/d3ddev.png)

<span data-ttu-id="0af0e-120">Direct3D 目前支援兩種主要類型的 Direct3D 裝置：</span><span class="sxs-lookup"><span data-stu-id="0af0e-120">Direct3D currently supports two main types of Direct3D devices:</span></span>

-   <span data-ttu-id="0af0e-121">具有硬體加速點陣化的 HAL 裝置，以及同時具有硬體和軟體頂點處理的著色</span><span class="sxs-lookup"><span data-stu-id="0af0e-121">A hal device with hardware-accelerated rasterization and shading with both hardware and software vertex processing</span></span>
-   <span data-ttu-id="0af0e-122">參照裝置</span><span class="sxs-lookup"><span data-stu-id="0af0e-122">A reference device</span></span>

<span data-ttu-id="0af0e-123">您可以將這些裝置視為兩個不同的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0af0e-123">You can think of these devices as two separate drivers.</span></span> <span data-ttu-id="0af0e-124">軟體與參照裝置是由軟體驅動程式表示，而 hal 裝置是由硬體驅動程式表示。</span><span class="sxs-lookup"><span data-stu-id="0af0e-124">Software and reference devices are represented by software drivers, and the hal device is represented by a hardware driver.</span></span> <span data-ttu-id="0af0e-125">利用這些裝置的最常見方式是使用 hal 裝置傳送應用程式，以及參照裝置用於功能測試。</span><span class="sxs-lookup"><span data-stu-id="0af0e-125">The most common way to take advantage of these devices is to use the hal device for shipping applications, and the reference device for feature testing.</span></span> <span data-ttu-id="0af0e-126">這些是由協力廠商提供，用來模擬特定裝置 - 例如尚未發行的開發中硬體。</span><span class="sxs-lookup"><span data-stu-id="0af0e-126">These are provided by third parties to emulate particular devices - for example, developmental hardware that has not yet been released.</span></span>

<span data-ttu-id="0af0e-127">應用程式建立的 Direct3D 裝置必須符合應用程式執行所在硬體的功能。</span><span class="sxs-lookup"><span data-stu-id="0af0e-127">The Direct3D device that an application creates must correspond to the capabilities of the hardware on which the application is running.</span></span> <span data-ttu-id="0af0e-128">Direct3D 提供轉譯功能，可透過存取電腦上安裝的 3D 硬體，或藉由模擬軟體中的 3D 硬體功能。</span><span class="sxs-lookup"><span data-stu-id="0af0e-128">Direct3D provides rendering capabilities, either by accessing 3D hardware that is installed in the computer or by emulating the capabilities of 3D hardware in software.</span></span> <span data-ttu-id="0af0e-129">因此，Direct3D 提供裝置同時用於硬體存取和軟體模擬。</span><span class="sxs-lookup"><span data-stu-id="0af0e-129">Therefore, Direct3D provides devices for both hardware access and software emulation.</span></span>

<span data-ttu-id="0af0e-130">硬體加速裝置提供的效能比軟體裝置好很多。</span><span class="sxs-lookup"><span data-stu-id="0af0e-130">Hardware-accelerated devices give much better performance than software devices.</span></span> <span data-ttu-id="0af0e-131">所有支援圖形卡的 Direct3D 上都提供 hal 裝置類型。</span><span class="sxs-lookup"><span data-stu-id="0af0e-131">The hal device type is available on all Direct3D supported graphic adapters.</span></span> <span data-ttu-id="0af0e-132">在大部分案例中，應用程式會以有硬體加速且依賴軟體模擬的電腦為目標，以配合較低階的電腦。</span><span class="sxs-lookup"><span data-stu-id="0af0e-132">In most cases, applications target computers that have hardware acceleration and rely on software emulation to accommodate lower-end computers.</span></span>

<span data-ttu-id="0af0e-133">參照裝置則例外，軟體裝置不一定與硬體裝置支援相同的功能。</span><span class="sxs-lookup"><span data-stu-id="0af0e-133">With the exception of the reference device, software devices do not always support the same features as a hardware device.</span></span> <span data-ttu-id="0af0e-134">應用程式應該永遠查詢裝置功能，以判斷支援哪些功能。</span><span class="sxs-lookup"><span data-stu-id="0af0e-134">Applications should always query for device capabilities to determine which features are supported.</span></span>

<span data-ttu-id="0af0e-135">由於 Direct3D 9 提供的軟體和參照裝置行為與 hal 裝置提供的相同，因此為搭配 hal 裝置所撰寫的應用程式程式碼將可搭配軟體或參照裝置運作，不需修改。</span><span class="sxs-lookup"><span data-stu-id="0af0e-135">Because the behavior of the software and reference devices provided with Direct3D 9 is identical to that of the hal device, application code authored to work with the hal device will work with the software or reference devices without modifications.</span></span> <span data-ttu-id="0af0e-136">請注意，雖然提供的軟體或參考裝置行為與 hal 裝置的行為完全相同，但裝置功能的確不同，而特定軟體裝置可能會執行一組較小的功能。</span><span class="sxs-lookup"><span data-stu-id="0af0e-136">Note that while the provided software or reference device behavior is identical to that of the hal device, the device capabilities do vary, and a particular software device may implement a much smaller set of capabilities.</span></span>

## <a name="behaviors"></a><span data-ttu-id="0af0e-137">行為</span><span class="sxs-lookup"><span data-stu-id="0af0e-137">Behaviors</span></span>

<span data-ttu-id="0af0e-138">Direct3D 可讓您指定裝置的行為，以及裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="0af0e-138">Direct3D enables you to specify the behavior of a device, as well the device's type.</span></span> <span data-ttu-id="0af0e-139">[**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)方法可結合一或多個行為旗標，以控制 Direct3D 裝置的全域行為。</span><span class="sxs-lookup"><span data-stu-id="0af0e-139">The [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method enables a combination of one or more of the behavior flags to control the global behaviors of the Direct3D device.</span></span> <span data-ttu-id="0af0e-140">這些行為會指定在 Direct3D 的執行時間部分中不會維護什麼，而且裝置類型會指定要使用的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0af0e-140">These behaviors specify what is and is not maintained in the run-time portion of Direct3D, and the device types specify which driver to use.</span></span> <span data-ttu-id="0af0e-141">雖然某些裝置行為組合無效，但您可以使用所有裝置類型的所有裝置行為。</span><span class="sxs-lookup"><span data-stu-id="0af0e-141">Although some combinations of device behaviors are not valid, it is possible to use all device behaviors with all device types.</span></span> <span data-ttu-id="0af0e-142">例如， \_ 在使用 D3DCREATE PUREDEVICE 建立的裝置上指定 D3DDEVTYPE SW 是有效的 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0af0e-142">For example, it is valid to specify D3DDEVTYPE\_SW on a device created with D3DCREATE\_PUREDEVICE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0af0e-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="0af0e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af0e-144">快速入門</span><span class="sxs-lookup"><span data-stu-id="0af0e-144">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 
