---
description: Direct3D 9 API 會根據安裝的作業系統，在 Windows XP 顯示驅動程式模型 ([) ] 或 [Windows Vista 顯示驅動程式模型 (WDDM) ] 上運作。
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM 和 WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991791"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="17ac8-103">XPDM 和 WDDM</span><span class="sxs-lookup"><span data-stu-id="17ac8-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="17ac8-104">Direct3D 9 API 會根據安裝的作業系統，在 Windows XP 顯示驅動程式模型 ([) ] 或 [Windows Vista 顯示驅動程式模型 (WDDM) ] 上運作。</span><span class="sxs-lookup"><span data-stu-id="17ac8-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="17ac8-105">Direct3D API 在兩個驅動程式模型上的運作方式有一些差異。</span><span class="sxs-lookup"><span data-stu-id="17ac8-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="17ac8-106">安全桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="17ac8-107">遠端桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="17ac8-108">Windows 服務</span><span class="sxs-lookup"><span data-stu-id="17ac8-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="17ac8-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="17ac8-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="17ac8-110">安全桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-110">Secure Desktop</span></span>

<span data-ttu-id="17ac8-111">只要發生下列任何一種情況，安全桌面就會處於作用中狀態：使用者將桌面鎖定 (Windows + L) 、螢幕保護裝置會在沒有使用者登入) 時啟動 (，或在使用者帳戶控制顯示提示時預設為啟用。</span><span class="sxs-lookup"><span data-stu-id="17ac8-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="17ac8-112">當安全桌面處於作用中狀態時，就無法存取 HAL 裝置。</span><span class="sxs-lookup"><span data-stu-id="17ac8-112">When the secure desktop is active, the HAL device is not accessible.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ac8-113">XPDM 和 WDDM 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="17ac8-113">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="17ac8-114">嘗試建立 Direct3D9 的 HAL 裝置會失敗 (**D3DERR \_ 無法 \_ 使用**) ，而且任何現有的 Direct3D 9 裝置都會指出目前遺失的裝置傳回碼。</span><span class="sxs-lookup"><span data-stu-id="17ac8-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span><br/> <span data-ttu-id="17ac8-115">Direct3D9Ex 和 Direct3D 10 Api 可以在安全桌面啟用時成功建立裝置，而且任何 ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) 或 DXGI) 的呼叫都會傳回狀態碼，指出桌面目前無法使用。</span><span class="sxs-lookup"><span data-stu-id="17ac8-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span><br/> |



 

## <a name="remote-desktop"></a><span data-ttu-id="17ac8-116">遠端桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-116">Remote Desktop</span></span>

<span data-ttu-id="17ac8-117">當遠端桌面處於作用中狀態時，顯示電腦會透過網路傳送資訊給主控電腦來處理。</span><span class="sxs-lookup"><span data-stu-id="17ac8-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ac8-118">XPDM 和 WDDM 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="17ac8-118">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="17ac8-119">在 XPDM 上，在遠端桌面上建立 Direct3D 9 裝置的所有嘗試都將失敗。</span><span class="sxs-lookup"><span data-stu-id="17ac8-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span><br/> <span data-ttu-id="17ac8-120">在 WDDM 中，遠端桌面支援透過遠端桌面會話建立 HAL 裝置。</span><span class="sxs-lookup"><span data-stu-id="17ac8-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span><br/> |



 

## <a name="windows-service"></a><span data-ttu-id="17ac8-121">Windows 服務</span><span class="sxs-lookup"><span data-stu-id="17ac8-121">Windows Service</span></span>

<span data-ttu-id="17ac8-122">Windows 服務是在背景中執行的處理常式，由服務控制管理員 (SCM) 控制。</span><span class="sxs-lookup"><span data-stu-id="17ac8-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="17ac8-123">服務會獨立于作用中的桌面執行，因此與使用者互動的能力有限。</span><span class="sxs-lookup"><span data-stu-id="17ac8-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ac8-124">XPDM 和 WDDM 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="17ac8-124">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="17ac8-125">在 WDDM 上，「會話0隔離」可確保服務無法存取任何使用者桌面做為安全性措施，因此，Windows 服務永遠不會提供 Direct3D 9 HAL 裝置。</span><span class="sxs-lookup"><span data-stu-id="17ac8-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="17ac8-126">您無法在 Windows 服務中使用 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="17ac8-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="17ac8-127">如需詳細資訊，請參閱 [Microsoft 支援文章 978635](https://support.microsoft.com/kb/978635)。</span><span class="sxs-lookup"><span data-stu-id="17ac8-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="17ac8-128">下表摘要說明此處所列的差異。</span><span class="sxs-lookup"><span data-stu-id="17ac8-128">The following table summarizes the differences listed here.</span></span>



|                 | <span data-ttu-id="17ac8-129">XPDM</span><span class="sxs-lookup"><span data-stu-id="17ac8-129">XPDM</span></span> | <span data-ttu-id="17ac8-130">WDDM (Direct3D9) </span><span class="sxs-lookup"><span data-stu-id="17ac8-130">WDDM (Direct3D9)</span></span> | <span data-ttu-id="17ac8-131">WDDM (Direct3D9Ex/Direct3D10) </span><span class="sxs-lookup"><span data-stu-id="17ac8-131">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="17ac8-132">安全桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-132">Secure Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="17ac8-133">NullREF</span><span class="sxs-lookup"><span data-stu-id="17ac8-133">NULLREF</span></span>         | <span data-ttu-id="17ac8-134">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-134">Yes</span></span>  | <span data-ttu-id="17ac8-135">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-135">Yes</span></span>              | <span data-ttu-id="17ac8-136">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-136">Yes</span></span>                          |
| <span data-ttu-id="17ac8-137">HAL</span><span class="sxs-lookup"><span data-stu-id="17ac8-137">HAL</span></span>             | <span data-ttu-id="17ac8-138">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-138">No</span></span>   | <span data-ttu-id="17ac8-139">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-139">No</span></span>               | <span data-ttu-id="17ac8-140">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-140">Yes</span></span>                          |
| <span data-ttu-id="17ac8-141">REF</span><span class="sxs-lookup"><span data-stu-id="17ac8-141">REF</span></span>             | <span data-ttu-id="17ac8-142">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-142">Yes</span></span>  | <span data-ttu-id="17ac8-143">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-143">Yes</span></span>              | <span data-ttu-id="17ac8-144">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-144">Yes</span></span>                          |
| <span data-ttu-id="17ac8-145">遠端桌面</span><span class="sxs-lookup"><span data-stu-id="17ac8-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="17ac8-146">NullREF</span><span class="sxs-lookup"><span data-stu-id="17ac8-146">NULLREF</span></span>         | <span data-ttu-id="17ac8-147">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-147">No</span></span>   | <span data-ttu-id="17ac8-148">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-148">Yes</span></span>              | <span data-ttu-id="17ac8-149">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-149">Yes</span></span>                          |
| <span data-ttu-id="17ac8-150">HAL</span><span class="sxs-lookup"><span data-stu-id="17ac8-150">HAL</span></span>             | <span data-ttu-id="17ac8-151">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-151">No</span></span>   | <span data-ttu-id="17ac8-152">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-152">Yes</span></span>              | <span data-ttu-id="17ac8-153">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-153">Yes</span></span>                          |
| <span data-ttu-id="17ac8-154">REF</span><span class="sxs-lookup"><span data-stu-id="17ac8-154">REF</span></span>             | <span data-ttu-id="17ac8-155">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-155">Yes</span></span>  | <span data-ttu-id="17ac8-156">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-156">Yes</span></span>              | <span data-ttu-id="17ac8-157">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-157">Yes</span></span>                          |
| <span data-ttu-id="17ac8-158">Windows 服務</span><span class="sxs-lookup"><span data-stu-id="17ac8-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="17ac8-159">NullREF</span><span class="sxs-lookup"><span data-stu-id="17ac8-159">NULLREF</span></span>         | <span data-ttu-id="17ac8-160">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-160">No</span></span>   | <span data-ttu-id="17ac8-161">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-161">No</span></span>               | <span data-ttu-id="17ac8-162">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-162">No</span></span>                           |
| <span data-ttu-id="17ac8-163">HAL</span><span class="sxs-lookup"><span data-stu-id="17ac8-163">HAL</span></span>             | <span data-ttu-id="17ac8-164">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-164">No</span></span>   | <span data-ttu-id="17ac8-165">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-165">No</span></span>               | <span data-ttu-id="17ac8-166">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-166">No</span></span>                           |
| <span data-ttu-id="17ac8-167">REF</span><span class="sxs-lookup"><span data-stu-id="17ac8-167">REF</span></span>             | <span data-ttu-id="17ac8-168">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-168">No</span></span>   | <span data-ttu-id="17ac8-169">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-169">No</span></span>               | <span data-ttu-id="17ac8-170">否</span><span class="sxs-lookup"><span data-stu-id="17ac8-170">No</span></span>                           |
| <span data-ttu-id="17ac8-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="17ac8-171">WARP10</span></span>          | <span data-ttu-id="17ac8-172">N/A</span><span class="sxs-lookup"><span data-stu-id="17ac8-172">N/A</span></span>  | <span data-ttu-id="17ac8-173">N/A</span><span class="sxs-lookup"><span data-stu-id="17ac8-173">N/A</span></span>              | <span data-ttu-id="17ac8-174">是</span><span class="sxs-lookup"><span data-stu-id="17ac8-174">Yes</span></span>                          |



 

<span data-ttu-id="17ac8-175">如需有關 XPDM、WDDM、Direct3D9Ex 和 Direct3D 10 的詳細資訊，請參閱 [Windows 中的圖形 api](../direct3darticles/graphics-apis-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="17ac8-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ac8-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="17ac8-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ac8-177">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="17ac8-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
