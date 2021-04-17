---
description: " (Direct3D 9) 的裝置類型"
ms.assetid: 860f3de2-beaf-4df1-82d0-a4b7508156c2
title: " (Direct3D 9) 的裝置類型"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84efe80c022403c36e760860893f3619e1c9356
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317627"
---
# <a name="device-types-direct3d-9"></a><span data-ttu-id="645f1-103"> (Direct3D 9) 的裝置類型</span><span class="sxs-lookup"><span data-stu-id="645f1-103">Device Types (Direct3D 9)</span></span>

## <a name="hal-device"></a><span data-ttu-id="645f1-104">HAL 裝置</span><span class="sxs-lookup"><span data-stu-id="645f1-104">HAL Device</span></span>

<span data-ttu-id="645f1-105">主要裝置類型是 hal 裝置，其支援硬體加速點陣化，以及硬體和軟體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="645f1-105">The primary device type is the hal device, which supports hardware accelerated rasterization and both hardware and software vertex processing.</span></span> <span data-ttu-id="645f1-106">如果您執行應用程式所在的電腦配備了支援 Direct3D 顯示卡，您的應用程式應該會使用它執行 Direct3D 作業。</span><span class="sxs-lookup"><span data-stu-id="645f1-106">If the computer on which your application is running is equipped with a display adapter that supports Direct3D, your application should use it for Direct3D operations.</span></span> <span data-ttu-id="645f1-107">Direct3D hal 裝置會實作硬體中的所有或部分轉換、光源和點陣化模組。</span><span class="sxs-lookup"><span data-stu-id="645f1-107">Direct3D hal devices implement all or part of the transformation, lighting, and rasterizing modules in hardware.</span></span>

<span data-ttu-id="645f1-108">應用程式不會直接存取圖形卡。</span><span class="sxs-lookup"><span data-stu-id="645f1-108">Applications do not access graphics adapters directly.</span></span> <span data-ttu-id="645f1-109">它們會呼叫 Direct3D 功能和方法。</span><span class="sxs-lookup"><span data-stu-id="645f1-109">They call Direct3D functions and methods.</span></span> <span data-ttu-id="645f1-110">Direct3D 會透過 hal 存取硬體。</span><span class="sxs-lookup"><span data-stu-id="645f1-110">Direct3D accesses the hardware through the hal.</span></span> <span data-ttu-id="645f1-111">如果您的應用程式執行所在的電腦支援 hal，它使用 hal 裝置將可獲得最佳效能。</span><span class="sxs-lookup"><span data-stu-id="645f1-111">If the computer that your application is running on supports the hal, it will gain the best performance by using a hal device.</span></span>

<span data-ttu-id="645f1-112">若要建立 hal 裝置，請[](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)使用 D3DDEVTYPE \_ hal 作為裝置類型來呼叫 CreateDevice。</span><span class="sxs-lookup"><span data-stu-id="645f1-112">To create a hal device, call [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) using D3DDEVTYPE\_HAL as the device type.</span></span>

## <a name="reference-device"></a><span data-ttu-id="645f1-113">參照裝置</span><span class="sxs-lookup"><span data-stu-id="645f1-113">Reference Device</span></span>

<span data-ttu-id="645f1-114">Direct3D 支援額外的裝置類型，稱為參照裝置或軟體模擬轉譯器。</span><span class="sxs-lookup"><span data-stu-id="645f1-114">Direct3D supports an additional device type called a reference device or reference rasterizer.</span></span> <span data-ttu-id="645f1-115">與軟體裝置不同的是，軟體模擬轉譯器支援每一項 Direct3D 功能。</span><span class="sxs-lookup"><span data-stu-id="645f1-115">Unlike a software device, the reference rasterizer supports every Direct3D feature.</span></span> <span data-ttu-id="645f1-116">此裝置主要用於偵錯，因此只在已安裝 DirectX SDK 的電腦上提供。</span><span class="sxs-lookup"><span data-stu-id="645f1-116">This device is intended to be used for debugging purposes and is therefore only available on machines where the DirectX SDK has been installed.</span></span> <span data-ttu-id="645f1-117">由於這些功能實作的目的在於精確性，而非速度，並且在軟體中實作，因此結果不會非常快。</span><span class="sxs-lookup"><span data-stu-id="645f1-117">Because these features are implemented for accuracy rather than speed and are implemented in software, the results are not very fast.</span></span> <span data-ttu-id="645f1-118">軟體模擬轉譯器確實會盡可能利用特殊 CPU 指令，但主要不是用於零售應用程式。</span><span class="sxs-lookup"><span data-stu-id="645f1-118">The reference rasterizer does make use of special CPU instructions whenever it can, but it is not intended for retail applications.</span></span> <span data-ttu-id="645f1-119">僅針對功能測試或展示目的使用軟體模擬轉譯器。</span><span class="sxs-lookup"><span data-stu-id="645f1-119">Use the reference rasterizer only for feature testing or demonstration purposes.</span></span> <span data-ttu-id="645f1-120">若要建立參考裝置，請[](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)使用 D3DDEVTYPE \_ REF 作為裝置類型來呼叫 CreateDevice 方法。</span><span class="sxs-lookup"><span data-stu-id="645f1-120">To create a reference device, call [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method using D3DDEVTYPE\_REF as the device type.</span></span>

## <a name="hal-vs-ref-devices"></a><span data-ttu-id="645f1-121">HAL 與參照裝置比較</span><span class="sxs-lookup"><span data-stu-id="645f1-121">HAL vs. REF Devices</span></span>

<span data-ttu-id="645f1-122">HAL (硬體抽象層) 裝置和 REF (軟體模擬轉譯器) 裝置是 Direct3D 裝置的主要兩種類型；第一種是以硬體支援為基礎，速度非常快，但可能不會提供全面支援；第二種則不會使用硬體加速，因此非常慢，但是保證支援完整的 Direct3D 功能，並採取正確的方式。</span><span class="sxs-lookup"><span data-stu-id="645f1-122">HAL (Hardware Abstraction Layer) devices and REF (REFerence rasterizer) devices are the two main types of Direct3D device; the first is based around the hardware support, and is very fast but might not support everything; while the second uses no hardware acceleration, so is very slow, but is guaranteed to support the entire set of Direct3D features, in the correct way.</span></span> <span data-ttu-id="645f1-123">一般來刷，您只會需要使用 HAL 裝置，但是如果您使用某些圖形卡不支援的進階功能，則您可能需要改用 REF。</span><span class="sxs-lookup"><span data-stu-id="645f1-123">In general you'll only ever need to use HAL devices, but if you're using some advanced feature that your graphics card does not support then you might need to fall back to REF.</span></span>

<span data-ttu-id="645f1-124">其他可能想要使用 REF 的情況是，如果 HAL 裝置產生奇怪的結果，也就是說，您確定程式碼是正確的，但結果卻不如預期。</span><span class="sxs-lookup"><span data-stu-id="645f1-124">The other time you might want to use REF is if the HAL device is producing strange results - that is, you're sure your code is correct, but the result is not what you're expecting.</span></span> <span data-ttu-id="645f1-125">REF 裝置保證會正確運作，因此您可能想要在 REF 裝置上測試應用程式，並查看奇怪的情形是否繼續發生。</span><span class="sxs-lookup"><span data-stu-id="645f1-125">The REF device is guaranteed to behave correctly, so you may wish to test your application on the REF device and see if the strange behavior continues.</span></span> <span data-ttu-id="645f1-126">如果未繼續發生，表示 (a) 您的應用程式假設圖形卡支援它應該不支援的項目，或 (b) 是驅動程式錯誤。</span><span class="sxs-lookup"><span data-stu-id="645f1-126">If it doesn't, it means that either (a) your application is assuming that the graphics card supports something that it doesn't, or (b) it's a driver bug.</span></span> <span data-ttu-id="645f1-127">如果使用 REF 裝置仍然無法運作，表示是應用程式錯誤。</span><span class="sxs-lookup"><span data-stu-id="645f1-127">If it still doesn't work with the REF device, then it's an application bug.</span></span>

## <a name="hardware-vs-software-vertex-processing"></a><span data-ttu-id="645f1-128">硬體與軟體頂點處理比較</span><span class="sxs-lookup"><span data-stu-id="645f1-128">Hardware vs. Software Vertex Processing</span></span>

<span data-ttu-id="645f1-129">硬體與軟體頂點處理僅適用於 HAL 裝置。</span><span class="sxs-lookup"><span data-stu-id="645f1-129">Hardware versus Software vertex processing only really applies to HAL devices.</span></span> <span data-ttu-id="645f1-130">當您透過管線推送頂點時，它們需要轉換 (輪流以世界、檢視、投影矩陣) 和照亮 (藉由 D3D 內建的照明) - 此處理階段稱為 T&L (代表轉換與光源)。</span><span class="sxs-lookup"><span data-stu-id="645f1-130">When you push vertices through the pipeline, they need to be transformed (by the world, view, and projection matrices in turn) and lit (by D3D's built-in lights) - this processing stage is known as T&L (for Transformation & Lighting).</span></span> <span data-ttu-id="645f1-131">硬體頂點處理表示是在硬體內完成 (如果硬體支援的話)；因此，軟體頂點處理是在軟體內完成。</span><span class="sxs-lookup"><span data-stu-id="645f1-131">Hardware vertex processing means this is done in hardware, if the hardware supports it; ergo, Software vertex processing is done is software.</span></span> <span data-ttu-id="645f1-132">一般方式是先嘗試建立硬體 T&L 裝置，如果失敗則嘗試混合，再失敗則嘗試軟體。</span><span class="sxs-lookup"><span data-stu-id="645f1-132">The general practice is to try creating a Hardware T&L device first, and if that fails try Mixed, and if that fails try Software.</span></span> <span data-ttu-id="645f1-133"> (如果軟體失敗，則放棄並退出) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="645f1-133">(If software fails, give up and exit with an error).</span></span>

## <a name="related-topics"></a><span data-ttu-id="645f1-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="645f1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="645f1-135">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="645f1-135">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
