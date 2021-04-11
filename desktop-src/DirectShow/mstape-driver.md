---
description: MSTape 驅動程式
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845755"
---
# <a name="mstape-driver"></a><span data-ttu-id="644ad-103">MSTape 驅動程式</span><span class="sxs-lookup"><span data-stu-id="644ad-103">MSTape Driver</span></span>

<span data-ttu-id="644ad-104">本主題適用于 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="644ad-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="644ad-105">MSTape 驅動程式支援 D-VHS 和 MPEG 攝像機裝置。</span><span class="sxs-lookup"><span data-stu-id="644ad-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="644ad-106">它會以 [WDM 影片捕獲](wdm-video-capture-filter.md) 篩選器的形式公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="644ad-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="644ad-107">它的功能與 [MSDV](msdv-driver.md)的 DV 攝像機驅動程式類似：</span><span class="sxs-lookup"><span data-stu-id="644ad-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="644ad-108">它會出現在「影片捕獲來源」 (CLSID \_ VideoInputDeviceCategory) 和「WDM 串流轉譯裝置」 (AM \_ KSCATEGORY 轉譯 \_) 篩選分類。</span><span class="sxs-lookup"><span data-stu-id="644ad-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="644ad-109">應用程式可以使用 [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) 介面來建立篩選準則的實例。</span><span class="sxs-lookup"><span data-stu-id="644ad-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="644ad-110">它具有用來從裝置進行捕捉和傳輸的輸出 pin，以及用於傳輸至裝置的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="644ad-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="644ad-111">一次只能連接一個 pin。</span><span class="sxs-lookup"><span data-stu-id="644ad-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="644ad-112">**媒體類型**</span><span class="sxs-lookup"><span data-stu-id="644ad-112">**Media Types**</span></span>

<span data-ttu-id="644ad-113">輸入 pin 支援一種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="644ad-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="644ad-114">主要類型</span><span class="sxs-lookup"><span data-stu-id="644ad-114">Major Type</span></span>   | <span data-ttu-id="644ad-115">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="644ad-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="644ad-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="644ad-116">Subtype</span></span>      | <span data-ttu-id="644ad-117">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="644ad-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="644ad-118">取樣大小</span><span class="sxs-lookup"><span data-stu-id="644ad-118">Sample Size</span></span>  | <span data-ttu-id="644ad-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="644ad-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="644ad-120">格式區塊</span><span class="sxs-lookup"><span data-stu-id="644ad-120">Format Block</span></span> | [<span data-ttu-id="644ad-121">**MPEG2 \_ 傳輸 \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="644ad-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="644ad-122">輸出 pin 支援兩種媒體類型。</span><span class="sxs-lookup"><span data-stu-id="644ad-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="644ad-123">主要類型</span><span class="sxs-lookup"><span data-stu-id="644ad-123">Major Type</span></span>   | <span data-ttu-id="644ad-124">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="644ad-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="644ad-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="644ad-125">Subtype</span></span>      | <span data-ttu-id="644ad-126">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="644ad-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="644ad-127">取樣大小</span><span class="sxs-lookup"><span data-stu-id="644ad-127">Sample Size</span></span>  | <span data-ttu-id="644ad-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="644ad-128">192 x 256</span></span>                              |
| <span data-ttu-id="644ad-129">格式區塊</span><span class="sxs-lookup"><span data-stu-id="644ad-129">Format Block</span></span> | <span data-ttu-id="644ad-130">MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="644ad-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="644ad-131">主要類型</span><span class="sxs-lookup"><span data-stu-id="644ad-131">Major Type</span></span>   | <span data-ttu-id="644ad-132">媒體媒體的 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="644ad-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="644ad-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="644ad-133">Subtype</span></span>      | <span data-ttu-id="644ad-134">MEDIASUBTYPE \_ MPEG2 \_ 傳輸 \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="644ad-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="644ad-135">取樣大小</span><span class="sxs-lookup"><span data-stu-id="644ad-135">Sample Size</span></span>  | <span data-ttu-id="644ad-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="644ad-136">188 x 256</span></span>                              |
| <span data-ttu-id="644ad-137">格式區塊</span><span class="sxs-lookup"><span data-stu-id="644ad-137">Format Block</span></span> | <span data-ttu-id="644ad-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="644ad-138">**NULL**</span></span>                               |



 

<span data-ttu-id="644ad-139">**裝置資訊**</span><span class="sxs-lookup"><span data-stu-id="644ad-139">**Device Information**</span></span>

<span data-ttu-id="644ad-140">驅動程式會動態讀取裝置設定 ROM 的資訊。</span><span class="sxs-lookup"><span data-stu-id="644ad-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="644ad-141">應用程式可以藉由將裝置的標記系結至屬性包，並呼叫 **IPropertyBag：： Read** 方法，來取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="644ad-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="644ad-142">屬性</span><span class="sxs-lookup"><span data-stu-id="644ad-142">Property</span></span>            | <span data-ttu-id="644ad-143">描述</span><span class="sxs-lookup"><span data-stu-id="644ad-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="644ad-144">資料類型</span><span class="sxs-lookup"><span data-stu-id="644ad-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="644ad-145">UniqueID \_ 低</span><span class="sxs-lookup"><span data-stu-id="644ad-145">UniqueID\_Low</span></span>       | <span data-ttu-id="644ad-146">裝置 (低 **DWORD**) 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="644ad-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="644ad-147">**long** (VT \_ I4) </span><span class="sxs-lookup"><span data-stu-id="644ad-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="644ad-148">UniqueID \_ 高</span><span class="sxs-lookup"><span data-stu-id="644ad-148">UniqueID\_High</span></span>      | <span data-ttu-id="644ad-149">裝置 (高 **DWORD**) 的唯一識別碼</span><span class="sxs-lookup"><span data-stu-id="644ad-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="644ad-150">**long**</span><span class="sxs-lookup"><span data-stu-id="644ad-150">**long**</span></span>            |
| <span data-ttu-id="644ad-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="644ad-151">VendorID</span></span>            | <span data-ttu-id="644ad-152">廠商識別碼。</span><span class="sxs-lookup"><span data-stu-id="644ad-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="644ad-153">**long**</span><span class="sxs-lookup"><span data-stu-id="644ad-153">**long**</span></span>            |
| <span data-ttu-id="644ad-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="644ad-154">ModelID</span></span>             | <span data-ttu-id="644ad-155">模型識別碼。</span><span class="sxs-lookup"><span data-stu-id="644ad-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="644ad-156">**long**</span><span class="sxs-lookup"><span data-stu-id="644ad-156">**long**</span></span>            |
| <span data-ttu-id="644ad-157">VendorText</span><span class="sxs-lookup"><span data-stu-id="644ad-157">VendorText</span></span>          | <span data-ttu-id="644ad-158">廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="644ad-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="644ad-159">**BSTR** (VT \_ bstr) </span><span class="sxs-lookup"><span data-stu-id="644ad-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="644ad-160">ModelText</span><span class="sxs-lookup"><span data-stu-id="644ad-160">ModelText</span></span>           | <span data-ttu-id="644ad-161">裝置型號名稱。</span><span class="sxs-lookup"><span data-stu-id="644ad-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="644ad-162">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="644ad-162">**BSTR**</span></span>            |
| <span data-ttu-id="644ad-163">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="644ad-163">UnitModelText</span></span>       | <span data-ttu-id="644ad-164">單位模型名稱;可能與 ModelText 相同。</span><span class="sxs-lookup"><span data-stu-id="644ad-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="644ad-165">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="644ad-165">**BSTR**</span></span>            |
| <span data-ttu-id="644ad-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="644ad-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="644ad-167">oPCR (輸出外掛程式控制項) 承載。</span><span class="sxs-lookup"><span data-stu-id="644ad-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="644ad-168">範例： 146 quadlets。</span><span class="sxs-lookup"><span data-stu-id="644ad-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="644ad-169">**long**</span><span class="sxs-lookup"><span data-stu-id="644ad-169">**long**</span></span>            |
| <span data-ttu-id="644ad-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="644ad-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="644ad-171">oPCR 資料速率。</span><span class="sxs-lookup"><span data-stu-id="644ad-171">oPCR data rate.</span></span> <span data-ttu-id="644ad-172">範例： 0 (S100) 、1 (S200) 或 2 (S400) 。</span><span class="sxs-lookup"><span data-stu-id="644ad-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="644ad-173">**long**</span><span class="sxs-lookup"><span data-stu-id="644ad-173">**long**</span></span>            |
| <span data-ttu-id="644ad-174">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="644ad-174">DeviceClassGUID</span></span>     | <span data-ttu-id="644ad-175">識別設備磁碟機的 GUID。</span><span class="sxs-lookup"><span data-stu-id="644ad-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="644ad-176">若為 MSTape，此值為 `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` 。</span><span class="sxs-lookup"><span data-stu-id="644ad-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="644ad-177">此 GUID 在標頭檔 Xprtdefs 中定義為 MSTapeDeviceGUID。</span><span class="sxs-lookup"><span data-stu-id="644ad-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="644ad-178">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="644ad-178">**BSTR**</span></span>            |
| <span data-ttu-id="644ad-179">Description</span><span class="sxs-lookup"><span data-stu-id="644ad-179">Description</span></span>         | <span data-ttu-id="644ad-180">從 INF 檔案取得之裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="644ad-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="644ad-181">此字串通常包含裝置的品牌名稱。</span><span class="sxs-lookup"><span data-stu-id="644ad-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="644ad-182">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="644ad-182">**BSTR**</span></span>            |



 

<span data-ttu-id="644ad-183">裝置識別碼是64位的整數。</span><span class="sxs-lookup"><span data-stu-id="644ad-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="644ad-184">低 **dword** 會儲存在 uniqueid \_ low 屬性中，而高 **Dword** 會儲存在 uniqueid \_ high 屬性中。</span><span class="sxs-lookup"><span data-stu-id="644ad-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="644ad-185">如需裝置名字標記的詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="644ad-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="644ad-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="644ad-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="644ad-187">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="644ad-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="644ad-188">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="644ad-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



