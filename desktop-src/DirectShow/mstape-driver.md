---
description: MSTape 驅動程式
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909396"
---
# <a name="mstape-driver"></a><span data-ttu-id="6b387-103">MSTape 驅動程式</span><span class="sxs-lookup"><span data-stu-id="6b387-103">MSTape Driver</span></span>

<span data-ttu-id="6b387-104">本主題適用于 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6b387-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="6b387-105">MSTape 驅動程式支援 D-VHS 和 MPEG 攝像機裝置。</span><span class="sxs-lookup"><span data-stu-id="6b387-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="6b387-106">它會以 [WDM 影片捕獲](wdm-video-capture-filter.md) 篩選器的形式公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="6b387-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="6b387-107">它的功能與 [MSDV](msdv-driver.md)的 DV 攝像機驅動程式類似：</span><span class="sxs-lookup"><span data-stu-id="6b387-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="6b387-108">它會出現在「影片捕獲來源」 (CLSID \_ VideoInputDeviceCategory) 和「WDM 串流轉譯裝置」 (AM \_ KSCATEGORY 轉譯 \_) 篩選分類。</span><span class="sxs-lookup"><span data-stu-id="6b387-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="6b387-109">應用程式可以使用 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面來建立篩選準則的實例。</span><span class="sxs-lookup"><span data-stu-id="6b387-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="6b387-110">它具有用來從裝置進行捕捉和傳輸的輸出 pin，以及用於傳輸至裝置的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="6b387-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="6b387-111">一次只能連接一個 pin。</span><span class="sxs-lookup"><span data-stu-id="6b387-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="6b387-112">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="6b387-112">**Media Types**</span></span>

<span data-ttu-id="6b387-113">輸入 pin 支援一種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b387-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="6b387-114">標籤</span><span class="sxs-lookup"><span data-stu-id="6b387-114">Label</span></span> | <span data-ttu-id="6b387-115">值</span><span class="sxs-lookup"><span data-stu-id="6b387-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="6b387-116">主要類型</span><span class="sxs-lookup"><span data-stu-id="6b387-116">Major Type</span></span>   | <span data-ttu-id="6b387-117">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="6b387-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="6b387-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="6b387-118">Subtype</span></span>      | <span data-ttu-id="6b387-119">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6b387-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="6b387-120">取樣大小</span><span class="sxs-lookup"><span data-stu-id="6b387-120">Sample Size</span></span>  | <span data-ttu-id="6b387-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="6b387-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="6b387-122">格式區塊</span><span class="sxs-lookup"><span data-stu-id="6b387-122">Format Block</span></span> | [<span data-ttu-id="6b387-123">**MPEG2 \_ 傳輸 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="6b387-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="6b387-124">輸出 pin 支援兩種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6b387-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="6b387-125">標籤</span><span class="sxs-lookup"><span data-stu-id="6b387-125">Label</span></span> | <span data-ttu-id="6b387-126">值</span><span class="sxs-lookup"><span data-stu-id="6b387-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="6b387-127">主要類型</span><span class="sxs-lookup"><span data-stu-id="6b387-127">Major Type</span></span>   | <span data-ttu-id="6b387-128">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="6b387-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="6b387-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="6b387-129">Subtype</span></span>      | <span data-ttu-id="6b387-130">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6b387-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="6b387-131">取樣大小</span><span class="sxs-lookup"><span data-stu-id="6b387-131">Sample Size</span></span>  | <span data-ttu-id="6b387-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="6b387-132">192 x 256</span></span>                              |
| <span data-ttu-id="6b387-133">格式區塊</span><span class="sxs-lookup"><span data-stu-id="6b387-133">Format Block</span></span> | <span data-ttu-id="6b387-134">MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6b387-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="6b387-135">標籤</span><span class="sxs-lookup"><span data-stu-id="6b387-135">Label</span></span> | <span data-ttu-id="6b387-136">值</span><span class="sxs-lookup"><span data-stu-id="6b387-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="6b387-137">主要類型</span><span class="sxs-lookup"><span data-stu-id="6b387-137">Major Type</span></span>   | <span data-ttu-id="6b387-138">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="6b387-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="6b387-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="6b387-139">Subtype</span></span>      | <span data-ttu-id="6b387-140">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="6b387-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="6b387-141">取樣大小</span><span class="sxs-lookup"><span data-stu-id="6b387-141">Sample Size</span></span>  | <span data-ttu-id="6b387-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="6b387-142">188 x 256</span></span>                              |
| <span data-ttu-id="6b387-143">格式區塊</span><span class="sxs-lookup"><span data-stu-id="6b387-143">Format Block</span></span> | <span data-ttu-id="6b387-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="6b387-144">**NULL**</span></span>                               |



 

<span data-ttu-id="6b387-145">**裝置資訊**</span><span class="sxs-lookup"><span data-stu-id="6b387-145">**Device Information**</span></span>

<span data-ttu-id="6b387-146">驅動程式會動態讀取裝置設定 ROM 的資訊。</span><span class="sxs-lookup"><span data-stu-id="6b387-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="6b387-147">應用程式可以藉由將裝置的標記系結至屬性包，並呼叫 **IPropertyBag：： Read** 方法，來取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="6b387-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="6b387-148">屬性</span><span class="sxs-lookup"><span data-stu-id="6b387-148">Property</span></span>            | <span data-ttu-id="6b387-149">描述</span><span class="sxs-lookup"><span data-stu-id="6b387-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="6b387-150">資料類型</span><span class="sxs-lookup"><span data-stu-id="6b387-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="6b387-151">UniqueID \_ 低</span><span class="sxs-lookup"><span data-stu-id="6b387-151">UniqueID\_Low</span></span>       | <span data-ttu-id="6b387-152">裝置 (低 **DWORD**) 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b387-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="6b387-153">**long** (VT \_ I4) </span><span class="sxs-lookup"><span data-stu-id="6b387-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="6b387-154">UniqueID \_ 高</span><span class="sxs-lookup"><span data-stu-id="6b387-154">UniqueID\_High</span></span>      | <span data-ttu-id="6b387-155">裝置 (高 **DWORD**) 的唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="6b387-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="6b387-156">**long**</span><span class="sxs-lookup"><span data-stu-id="6b387-156">**long**</span></span>            |
| <span data-ttu-id="6b387-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="6b387-157">VendorID</span></span>            | <span data-ttu-id="6b387-158">廠商識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b387-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="6b387-159">**long**</span><span class="sxs-lookup"><span data-stu-id="6b387-159">**long**</span></span>            |
| <span data-ttu-id="6b387-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="6b387-160">ModelID</span></span>             | <span data-ttu-id="6b387-161">模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b387-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="6b387-162">**long**</span><span class="sxs-lookup"><span data-stu-id="6b387-162">**long**</span></span>            |
| <span data-ttu-id="6b387-163">VendorText</span><span class="sxs-lookup"><span data-stu-id="6b387-163">VendorText</span></span>          | <span data-ttu-id="6b387-164">廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="6b387-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="6b387-165">**BSTR** (VT \_ bstr) </span><span class="sxs-lookup"><span data-stu-id="6b387-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="6b387-166">ModelText</span><span class="sxs-lookup"><span data-stu-id="6b387-166">ModelText</span></span>           | <span data-ttu-id="6b387-167">裝置型號名稱。</span><span class="sxs-lookup"><span data-stu-id="6b387-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="6b387-168">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b387-168">**BSTR**</span></span>            |
| <span data-ttu-id="6b387-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="6b387-169">UnitModelText</span></span>       | <span data-ttu-id="6b387-170">單位模型名稱;可能與 ModelText 相同。</span><span class="sxs-lookup"><span data-stu-id="6b387-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="6b387-171">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b387-171">**BSTR**</span></span>            |
| <span data-ttu-id="6b387-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="6b387-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="6b387-173">oPCR (輸出外掛程式控制項) 承載。</span><span class="sxs-lookup"><span data-stu-id="6b387-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="6b387-174">範例： 146 quadlets。</span><span class="sxs-lookup"><span data-stu-id="6b387-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="6b387-175">**long**</span><span class="sxs-lookup"><span data-stu-id="6b387-175">**long**</span></span>            |
| <span data-ttu-id="6b387-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="6b387-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="6b387-177">oPCR 資料速率。</span><span class="sxs-lookup"><span data-stu-id="6b387-177">oPCR data rate.</span></span> <span data-ttu-id="6b387-178">範例： 0 (S100) 、1 (S200) 或 2 (S400) 。</span><span class="sxs-lookup"><span data-stu-id="6b387-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="6b387-179">**long**</span><span class="sxs-lookup"><span data-stu-id="6b387-179">**long**</span></span>            |
| <span data-ttu-id="6b387-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="6b387-180">DeviceClassGUID</span></span>     | <span data-ttu-id="6b387-181">識別設備磁碟機的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6b387-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="6b387-182">若為 MSTape，此值為 `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` 。</span><span class="sxs-lookup"><span data-stu-id="6b387-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="6b387-183">此 GUID 在標頭檔 Xprtdefs 中定義為 MSTapeDeviceGUID。</span><span class="sxs-lookup"><span data-stu-id="6b387-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="6b387-184">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b387-184">**BSTR**</span></span>            |
| <span data-ttu-id="6b387-185">Description</span><span class="sxs-lookup"><span data-stu-id="6b387-185">Description</span></span>         | <span data-ttu-id="6b387-186">從 INF 檔案取得之裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="6b387-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="6b387-187">此字串通常包含裝置的品牌名稱。</span><span class="sxs-lookup"><span data-stu-id="6b387-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="6b387-188">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="6b387-188">**BSTR**</span></span>            |



 

<span data-ttu-id="6b387-189">裝置識別碼是64位的整數。</span><span class="sxs-lookup"><span data-stu-id="6b387-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="6b387-190">低 **dword** 會儲存在 uniqueid \_ low 屬性中，而高 **Dword** 會儲存在 uniqueid \_ high 屬性中。</span><span class="sxs-lookup"><span data-stu-id="6b387-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="6b387-191">如需裝置名字標記的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="6b387-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b387-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b387-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b387-193">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="6b387-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="6b387-194">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="6b387-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



