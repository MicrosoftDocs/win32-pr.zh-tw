---
description: 瞭解列印架構中的使用者可設定關鍵字，以進行色彩管理，例如 PageColorManagement 和 PageBlackGenerationProcessing。
ms.assetid: 296255b8-fe5c-46dd-b717-487aaae0db80
title: 色彩管理和列印架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9258d9dcc59ab24f9cfca8e170bf3f3f62841b21
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409671"
---
# <a name="color-management-and-the-print-schema"></a><span data-ttu-id="47a50-103">色彩管理和列印架構</span><span class="sxs-lookup"><span data-stu-id="47a50-103">Color Management and the Print Schema</span></span>

<span data-ttu-id="47a50-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="47a50-104">This topic is not current.</span></span> <span data-ttu-id="47a50-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="47a50-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="47a50-106">使用者可設定的元素關鍵字可以是 XPS 專屬或非 XPS 特定。</span><span class="sxs-lookup"><span data-stu-id="47a50-106">User Configurable Element keywords may either be XPS specific or non-XPS specific.</span></span> <span data-ttu-id="47a50-107">如果它們不是 XPS 專用，關鍵字可能會用於舊版的 GDI 式列印。</span><span class="sxs-lookup"><span data-stu-id="47a50-107">In the case where they are not XPS specific, the keyword may be used for Legacy GDI-based printing.</span></span> <span data-ttu-id="47a50-108">如果應用程式決定在 PrintTicket 中設定這些關鍵字，驅動程式會根據列印架構中所呈現的定義，決定要採取的適當動作和行為。</span><span class="sxs-lookup"><span data-stu-id="47a50-108">If an application decides to set these keywords in a PrintTicket, it is up to the driver to determine the proper action and behavior to take based on the definitions presented in the Print Schema.</span></span> <span data-ttu-id="47a50-109">任何這些關鍵字都可用於 ICM 的內容中。</span><span class="sxs-lookup"><span data-stu-id="47a50-109">Any of these keywords may be used in the context of ICM.</span></span> <span data-ttu-id="47a50-110">如需詳細資訊，請參閱 Windows Vista SDK。</span><span class="sxs-lookup"><span data-stu-id="47a50-110">For more information, please see the Windows Vista SDK.</span></span>



| <span data-ttu-id="47a50-111">列印架構使用者可設定關鍵字</span><span class="sxs-lookup"><span data-stu-id="47a50-111">Print Schema User Configurable Keyword</span></span>       | <span data-ttu-id="47a50-112">DEVMODE 相等</span><span class="sxs-lookup"><span data-stu-id="47a50-112">DEVMODE Equivalent</span></span>     | <span data-ttu-id="47a50-113">XPS 特定</span><span class="sxs-lookup"><span data-stu-id="47a50-113">XPS Specific</span></span>   |
|----------------------------------------------|------------------------|----------------|
| <span data-ttu-id="47a50-114">PageColorManagement</span><span class="sxs-lookup"><span data-stu-id="47a50-114">PageColorManagement</span></span><br/>               | <span data-ttu-id="47a50-115">dmICMMethod</span><span class="sxs-lookup"><span data-stu-id="47a50-115">dmICMMethod</span></span><br/> | <span data-ttu-id="47a50-116">否</span><span class="sxs-lookup"><span data-stu-id="47a50-116">No</span></span><br/>  |
| <span data-ttu-id="47a50-117">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="47a50-117">PageBlackGenerationProcessing</span></span><br/>     | <span data-ttu-id="47a50-118">無</span><span class="sxs-lookup"><span data-stu-id="47a50-118">None</span></span><br/>        | <span data-ttu-id="47a50-119">是</span><span class="sxs-lookup"><span data-stu-id="47a50-119">Yes</span></span><br/> |
| <span data-ttu-id="47a50-120">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="47a50-120">PageBlendColorSpace</span></span><br/>               | <span data-ttu-id="47a50-121">無</span><span class="sxs-lookup"><span data-stu-id="47a50-121">None</span></span><br/>        | <span data-ttu-id="47a50-122">是</span><span class="sxs-lookup"><span data-stu-id="47a50-122">Yes</span></span><br/> |
| <span data-ttu-id="47a50-123">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="47a50-123">PageSourceColorProfile</span></span><br/>            | <span data-ttu-id="47a50-124">無</span><span class="sxs-lookup"><span data-stu-id="47a50-124">None</span></span><br/>        | <span data-ttu-id="47a50-125">否</span><span class="sxs-lookup"><span data-stu-id="47a50-125">No</span></span><br/>  |
| <span data-ttu-id="47a50-126">PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="47a50-126">PageDestinationColorProfile</span></span><br/>       | <span data-ttu-id="47a50-127">無</span><span class="sxs-lookup"><span data-stu-id="47a50-127">None</span></span><br/>        | <span data-ttu-id="47a50-128">否</span><span class="sxs-lookup"><span data-stu-id="47a50-128">No</span></span><br/>  |
| <span data-ttu-id="47a50-129">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="47a50-129">PageICMRenderingIntent</span></span><br/>            | <span data-ttu-id="47a50-130">dmICMIntent</span><span class="sxs-lookup"><span data-stu-id="47a50-130">dmICMIntent</span></span><br/> | <span data-ttu-id="47a50-131">否</span><span class="sxs-lookup"><span data-stu-id="47a50-131">No</span></span><br/>  |
| <span data-ttu-id="47a50-132">JobOptimalDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="47a50-132">JobOptimalDestinationColorProfile</span></span><br/> | <span data-ttu-id="47a50-133">無</span><span class="sxs-lookup"><span data-stu-id="47a50-133">None</span></span><br/>        | <span data-ttu-id="47a50-134">否</span><span class="sxs-lookup"><span data-stu-id="47a50-134">No</span></span><br/>  |
| <span data-ttu-id="47a50-135">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="47a50-135">PageDeviceColorSpaceUsage</span></span><br/>         | <span data-ttu-id="47a50-136">無</span><span class="sxs-lookup"><span data-stu-id="47a50-136">None</span></span><br/>        | <span data-ttu-id="47a50-137">是</span><span class="sxs-lookup"><span data-stu-id="47a50-137">Yes</span></span><br/> |



 

## <a name="pagecolormanagement-system-handling"></a><span data-ttu-id="47a50-138">PageColorManagement 系統處理</span><span class="sxs-lookup"><span data-stu-id="47a50-138">PageColorManagement System Handling</span></span>

<span data-ttu-id="47a50-139">若為 PageColorManagement，系統會提供自動處理 PrintTicket 至 DEVMODE 或 DEVMODE 轉換（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="47a50-139">For PageColorManagement, the system provides automatic handling of PrintTicket to DEVMODE or DEVMODE to PrintTicket conversion if necessary.</span></span> <span data-ttu-id="47a50-140">這取決於應用程式 (Win32 或 WPF) 之間的特定列印路徑，以及 (以 GDI 為基礎或 XPSDrv) 的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="47a50-140">This depends on the specific print path between the application (Win32 or WPF)and the driver (GDI-based or XPSDrv).</span></span> <span data-ttu-id="47a50-141">如果從 Windows Presentation Foundation 應用程式列印到 Microsoft XPSDrv 列印驅動程式，則不應在 PrintTicket 或 PrintCapabilities 檔中通告系統的 PageColorManagement 公用選項;在此情況下，系統無法自動處理色彩管理。</span><span class="sxs-lookup"><span data-stu-id="47a50-141">In the case of printing from a Windows Presentation Foundation application to a Microsoft XPSDrv print driver, a PageColorManagement public option of System SHOULD NOT be advertised in either the PrintTicket or PrintCapabilities document; in this case, color management cannot be handled automatically by the system.</span></span> <span data-ttu-id="47a50-142">從 Win32 應用程式列印到 Microsoft XPSDrv 列印驅動程式，可能會導致應用程式與 GDI 之間的色彩管理不過，在轉換成 XPS 格式之後，XPS 檔與驅動程式和/或裝置之間將不會自動處理色彩管理的系統，因為 XPS 格式標記每個元素都有完整的色彩資訊，而且會由驅動程式或裝置來處理此資訊。</span><span class="sxs-lookup"><span data-stu-id="47a50-142">Printing from a Win32 application to a Microsoft XPSDrv print driver may result in color management between the application and GDI, however after conversion to XPS-format, there will be no automatic system handling of color management between the XPS document and the driver and/or device, because the XPS-format tags each element with complete color information, and it is up to the driver or the device to process this information.</span></span>



| <span data-ttu-id="47a50-143">PageColorManagement 公用選項</span><span class="sxs-lookup"><span data-stu-id="47a50-143">PageColorManagement Public Options</span></span> | <span data-ttu-id="47a50-144">DEVMODE 值</span><span class="sxs-lookup"><span data-stu-id="47a50-144">DEVMODE Value</span></span>                  |
|------------------------------------|--------------------------------|
| <span data-ttu-id="47a50-145">無</span><span class="sxs-lookup"><span data-stu-id="47a50-145">None</span></span><br/>                    | <span data-ttu-id="47a50-146">DMICMMETHOD \_ 無</span><span class="sxs-lookup"><span data-stu-id="47a50-146">DMICMMETHOD\_NONE</span></span><br/>   |
| <span data-ttu-id="47a50-147">裝置</span><span class="sxs-lookup"><span data-stu-id="47a50-147">Device</span></span><br/>                  | <span data-ttu-id="47a50-148">DMICMMETHOD \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="47a50-148">DMICMMETHOD\_DEVICE</span></span><br/> |
| <span data-ttu-id="47a50-149">驅動程式</span><span class="sxs-lookup"><span data-stu-id="47a50-149">Driver</span></span><br/>                  | <span data-ttu-id="47a50-150">DMICMMETHOD \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="47a50-150">DMICMMETHOD\_DRIVER</span></span><br/> |
| <span data-ttu-id="47a50-151">系統</span><span class="sxs-lookup"><span data-stu-id="47a50-151">System</span></span><br/>                  | <span data-ttu-id="47a50-152">DMICMMETHOD \_ 系統</span><span class="sxs-lookup"><span data-stu-id="47a50-152">DMICMMETHOD\_SYSTEM</span></span><br/> |



 

## <a name="pageicmrenderingintent-system-handling"></a><span data-ttu-id="47a50-153">PageICMRenderingIntent 系統處理</span><span class="sxs-lookup"><span data-stu-id="47a50-153">PageICMRenderingIntent System Handling</span></span>

<span data-ttu-id="47a50-154">若為 PageICMRenderingIntent，系統會提供自動處理 PrintTicket 至 DEVMODE 或 DEVMODE 轉換（如有必要）。</span><span class="sxs-lookup"><span data-stu-id="47a50-154">For PageICMRenderingIntent, the system provides automatic handling of PrintTicket to DEVMODE or DEVMODE to PrintTicket conversion if necessary.</span></span> <span data-ttu-id="47a50-155">這取決於應用程式 (Win32 或 Windows Presentation Foundation) 之間的特定列印路徑，以及 (以 GDI 為基礎或 XPSDrv) 的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="47a50-155">This depends on the specific print path between the application (Win32 or Windows Presentation Foundation) and the driver (GDI-based or XPSDrv).</span></span>



| <span data-ttu-id="47a50-156">PageICMRenderingIntent 公用選項</span><span class="sxs-lookup"><span data-stu-id="47a50-156">PageICMRenderingIntent Public Options</span></span> | <span data-ttu-id="47a50-157">DEVMODE 值</span><span class="sxs-lookup"><span data-stu-id="47a50-157">DEVMODE Value</span></span>                       |
|---------------------------------------|-------------------------------------|
| <span data-ttu-id="47a50-158">AbsoluteColorimetric</span><span class="sxs-lookup"><span data-stu-id="47a50-158">AbsoluteColorimetric</span></span><br/>       | <span data-ttu-id="47a50-159">DMICM \_ ABS \_ 色度</span><span class="sxs-lookup"><span data-stu-id="47a50-159">DMICM\_ABS\_COLORIMETRIC</span></span><br/> |
| <span data-ttu-id="47a50-160">RelativeColorimetric</span><span class="sxs-lookup"><span data-stu-id="47a50-160">RelativeColorimetric</span></span><br/>       | <span data-ttu-id="47a50-161">DMICM \_ 色度</span><span class="sxs-lookup"><span data-stu-id="47a50-161">DMICM\_COLORIMETRIC</span></span><br/>      |
| <span data-ttu-id="47a50-162">照片</span><span class="sxs-lookup"><span data-stu-id="47a50-162">Photographs</span></span><br/>                | <span data-ttu-id="47a50-163">DMICM \_ 對比</span><span class="sxs-lookup"><span data-stu-id="47a50-163">DMICM\_CONTRAST</span></span><br/>          |
| <span data-ttu-id="47a50-164">BusinessGraphics</span><span class="sxs-lookup"><span data-stu-id="47a50-164">BusinessGraphics</span></span><br/>           | <span data-ttu-id="47a50-165">DMICM \_ 飽和</span><span class="sxs-lookup"><span data-stu-id="47a50-165">DMICM\_SATURATE</span></span><br/>          |



 

<span data-ttu-id="47a50-166">除了 PageColorManagement 或) PageICMRenderingIntent 以外，其他所有色彩管理相關關鍵字 (不會有這類自動處理。</span><span class="sxs-lookup"><span data-stu-id="47a50-166">All other Color Management related keywords (besides PageColorManagement or PageICMRenderingIntent) do not have such automatic handling.</span></span>

## <a name="joboptimaldestinationcolorprofile-and-pagedestinationcolorprofile-usage"></a><span data-ttu-id="47a50-167">JobOptimalDestinationColorProfile 和 PageDestinationColorProfile 使用量</span><span class="sxs-lookup"><span data-stu-id="47a50-167">JobOptimalDestinationColorProfile and PageDestinationColorProfile Usage</span></span>

<span data-ttu-id="47a50-168">應用程式可能會決定查詢 PrintCapabilities 檔以進行 JobOptimalDestinationColorProfile。</span><span class="sxs-lookup"><span data-stu-id="47a50-168">An application MAY decide to query PrintCapabilities document for JobOptimalDestinationColorProfile.</span></span> <span data-ttu-id="47a50-169">這可為應用程式提供最佳色彩設定檔，提供 PrintCapabilities 檔中定義的目前裝置設定。</span><span class="sxs-lookup"><span data-stu-id="47a50-169">This could give an application the optimal color profile given the current device configuration as defined in the PrintCapabilities document.</span></span> <span data-ttu-id="47a50-170">如果應用程式決定要讓驅動程式對 JobOptimalDestinationColorProfile 所指定的目的地色彩設定檔執行色彩管理，則 PageColorManagement 和 PageDestinationColorProfile 會分別設定為 [驅動程式] 和 [DriverConfiguration]。</span><span class="sxs-lookup"><span data-stu-id="47a50-170">If the application decides it would like the driver to perform color management to the destination color profile specified by JobOptimalDestinationColorProfile, then PageColorManagement and PageDestinationColorProfile would be set to Driver and DriverConfiguration in the PrintTicket respectively.</span></span> <span data-ttu-id="47a50-171">如果應用程式不想使用 JobOptionalDestinationColorProfile 並選擇使用它自己的，則應該將 PageColorManagement 設定為 [無]，並將 PageDestinationColorProfile 設定為 PrintTicket 中的 [應用程式]，以傳達應用程式已經對其指定的目的地色彩設定檔執行色彩管理。</span><span class="sxs-lookup"><span data-stu-id="47a50-171">If the application does not want to use the JobOptionalDestinationColorProfile and chooses to use its own, it SHOULD set PageColorManagement to None and also set the PageDestinationColorProfile to Application in the PrintTicket to convey that the application has already performed color management to its specified destination color profile.</span></span> <span data-ttu-id="47a50-172">另一種情況可能會在應用程式選擇使用驅動程式 PrintCapabilities 所傳回的最佳目的地色彩設定檔時，但決定自行進行色彩管理時也會發生。</span><span class="sxs-lookup"><span data-stu-id="47a50-172">Another scenario may occur when the application chooses to use the optimal destination color profile returned by the drivers PrintCapabilities but decides to do color management on its own.</span></span> <span data-ttu-id="47a50-173">在此情況下，PageColorManagement 會設定為 [無]，而 PageDestinationColorProfile 會設定為 [應用程式]。</span><span class="sxs-lookup"><span data-stu-id="47a50-173">In this case, PageColorManagement would be set to None and PageDestinationColorProfile would be set to Application.</span></span>

## <a name="pagesourcecolorprofile-usage"></a><span data-ttu-id="47a50-174">PageSourceColorProfile 使用方式</span><span class="sxs-lookup"><span data-stu-id="47a50-174">PageSourceColorProfile Usage</span></span>

<span data-ttu-id="47a50-175">針對 PageSourceColorProfile，無論針對 PageColorManagement 選取的選項為何，應用程式都可以針對 PrintTicket 中的每個頁面指定來源色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="47a50-175">For PageSourceColorProfile, an application MAY specify a source color profile for each page in the PrintTicket, regardless of the option selected for PageColorManagement.</span></span> <span data-ttu-id="47a50-176">無論是否存在，驅動程式都會根據列印架構中所呈現的定義，決定每個案例的行為。</span><span class="sxs-lookup"><span data-stu-id="47a50-176">Whether it is present or not, it is up to the driver to decide the behavior for each case based on the definitions presented in the Print Schema.</span></span> <span data-ttu-id="47a50-177">例如，應用程式可能會將 PageColorManagement 設定為 None，然後未在 PrintTicket 中設定 PageSourceColorProfile。</span><span class="sxs-lookup"><span data-stu-id="47a50-177">For example, an application may set PageColorManagement to None, and then not set PageSourceColorProfile in the PrintTicket.</span></span> <span data-ttu-id="47a50-178">應用程式也可以設定 PageColorManagement 至驅動程式，然後在 PrintTicket 中設定 PageSourceColorProfile;在此情況下，此驅動程式會負責判斷 PrintSchema 指導方針內的行為。</span><span class="sxs-lookup"><span data-stu-id="47a50-178">It is also possible for an application to set PageColorManagement to Driver, and then set PageSourceColorProfile in the PrintTicket; the driver in this case is responsible for determining the behavior within the guidelines of the PrintSchema.</span></span>

## <a name="pagedevicecolorspaceusage"></a><span data-ttu-id="47a50-179">PageDeviceColorSpaceUsage</span><span class="sxs-lookup"><span data-stu-id="47a50-179">PageDeviceColorSpaceUsage</span></span>

<span data-ttu-id="47a50-180">PageDeviceColorSpaceUsage 是應用程式所設定的 XPS 特定使用者可設定元素。</span><span class="sxs-lookup"><span data-stu-id="47a50-180">PageDeviceColorSpaceUsage is an XPS specific user configurable element that is set by the application.</span></span> <span data-ttu-id="47a50-181">它會針對 XPS 檔中相關聯的色彩空間設定檔處理，在 PrintTicket 中設定適當的選項，以提供裝置的指示。</span><span class="sxs-lookup"><span data-stu-id="47a50-181">It provides instructions for the device by setting the appropriate option in the PrintTicket, for color space profile handling associated within an XPS document.</span></span> <span data-ttu-id="47a50-182">應用程式和/或現有的 PrintTicket 可以在傳送至裝置的 PrintTicket 中指定這個關鍵字。</span><span class="sxs-lookup"><span data-stu-id="47a50-182">The application and/or existing PrintTicket MAY specify this keyword in a PrintTicket sent to the device.</span></span> <span data-ttu-id="47a50-183">無論是否存在，驅動程式都會根據列印架構中所呈現的定義，決定每個案例的行為。</span><span class="sxs-lookup"><span data-stu-id="47a50-183">Whether it is present or not, it is up to the driver to decide the behavior for each case, based on the definitions presented in the Print Schema.</span></span>

## <a name="print-schema-color-management-example-flow"></a><span data-ttu-id="47a50-184">列印架構色彩管理範例流程</span><span class="sxs-lookup"><span data-stu-id="47a50-184">Print Schema Color Management Example Flow</span></span>

<span data-ttu-id="47a50-185">下圖說明使用色彩管理和列印架構的最可能案例的流程。</span><span class="sxs-lookup"><span data-stu-id="47a50-185">The following diagram illustrates flow for the most likely scenarios for using Color Management and the Print Schema.</span></span> <span data-ttu-id="47a50-186">為了簡化和可讀性，只有下列使用者可設定的列印架構關鍵字會用來示範其使用方式： PageColorManagement、JobOptimalDestinaionColorProfile、PageSourceColorProfile 和 PageDestinationColorProfile。</span><span class="sxs-lookup"><span data-stu-id="47a50-186">For simplicity and readability, only the following user configurable Print Schema keywords were used to demonstrate their usage: PageColorManagement, JobOptimalDestinaionColorProfile, PageSourceColorProfile, and PageDestinationColorProfile.</span></span> <span data-ttu-id="47a50-187">實線表示應該發生的動作，而虛線表示可能會發生的動作。</span><span class="sxs-lookup"><span data-stu-id="47a50-187">A solid line represents an action that SHOULD occur and a dashed line represents an action that MAY occur.</span></span> <span data-ttu-id="47a50-188">下列案例不是會在應用程式、驅動程式和系統之間產生的保證互動，而是代表將會發生的最常見使用案例。</span><span class="sxs-lookup"><span data-stu-id="47a50-188">The following scenario is not the guaranteed interaction that will result between the application, driver, and system, however, it represents the most common usage case that will occur.</span></span>

![顯示如何處理色彩管理設定的圖表](images/local-1992284846-colormanagementtest3.png)

## <a name="related-topics"></a><span data-ttu-id="47a50-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="47a50-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a50-191">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="47a50-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




