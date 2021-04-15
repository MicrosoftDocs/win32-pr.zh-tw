---
description: Windows 映像取得 (WIA) 是 Windows 系列作業系統的靜止映射取得平臺，從 Windows Millennium Edition (Windows Me) 和 Windows XP 起。
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Windows Image Acquisition (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff1f3fb51a4c87d909637a90591336d9d2eb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511608"
---
# <a name="windows-image-acquisition-wia"></a><span data-ttu-id="8286e-103">Windows Image Acquisition (WIA)</span><span class="sxs-lookup"><span data-stu-id="8286e-103">Windows Image Acquisition (WIA)</span></span>

<span data-ttu-id="8286e-104">Windows 映像取得 (WIA) 是 Windows 系列作業系統的靜止映射取得平臺，從 Windows Millennium Edition (Windows Me) 和 Windows XP 起。</span><span class="sxs-lookup"><span data-stu-id="8286e-104">Windows Image Acquisition (WIA) is the still image acquisition platform in the Windows family of operating systems starting with Windows Millennium Edition (Windows Me) and Windows XP.</span></span>

-   [<span data-ttu-id="8286e-105">簡介</span><span class="sxs-lookup"><span data-stu-id="8286e-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8286e-106">Windows 映像收購2.0 的優點</span><span class="sxs-lookup"><span data-stu-id="8286e-106">Benefits of Windows Image Acquisition 2.0</span></span>](#benefits-of-windows-image-acquisition-20)
    -   [<span data-ttu-id="8286e-107">針對應用程式寫入器</span><span class="sxs-lookup"><span data-stu-id="8286e-107">For Application Writers</span></span>](#for-application-writers)
    -   [<span data-ttu-id="8286e-108">針對裝置製造商</span><span class="sxs-lookup"><span data-stu-id="8286e-108">For Device Manufactures</span></span>](#for-device-manufactures)
    -   [<span data-ttu-id="8286e-109">針對掃描器使用者</span><span class="sxs-lookup"><span data-stu-id="8286e-109">For Scanner Users</span></span>](#for-scanner-users)
-   [<span data-ttu-id="8286e-110">開發 Windows 映像</span><span class="sxs-lookup"><span data-stu-id="8286e-110">Development of Windows Image Acquisition</span></span>](#development-of-windows-image-acquisition)
-   [<span data-ttu-id="8286e-111">Windows 映像取得簡介</span><span class="sxs-lookup"><span data-stu-id="8286e-111">Overview of Windows Image Acquisition</span></span>](#overview-of-windows-image-acquisition)
-   [<span data-ttu-id="8286e-112">Windows 映像取得2.0 的相關事實</span><span class="sxs-lookup"><span data-stu-id="8286e-112">Facts about Windows Image Acquisition 2.0</span></span>](#facts-about-windows-image-acquisition-20)
-   [<span data-ttu-id="8286e-113">開發人員物件</span><span class="sxs-lookup"><span data-stu-id="8286e-113">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="8286e-114">執行時間需求</span><span class="sxs-lookup"><span data-stu-id="8286e-114">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="8286e-115">WIA 主題</span><span class="sxs-lookup"><span data-stu-id="8286e-115">WIA Topics</span></span>](#wia-topics)

## <a name="introduction"></a><span data-ttu-id="8286e-116">簡介</span><span class="sxs-lookup"><span data-stu-id="8286e-116">Introduction</span></span>

<span data-ttu-id="8286e-117">WIA 平臺可讓影像處理/圖形應用程式與映射處理硬體互動，並將不同應用程式和掃描器之間的互動標準化。</span><span class="sxs-lookup"><span data-stu-id="8286e-117">The WIA platform enables imaging/graphics applications to interact with imaging hardware and standardizes the interaction between different applications and scanners.</span></span> <span data-ttu-id="8286e-118">這可讓那些不同的應用程式與這些不同的掃描器交談並進行互動，而不需要應用程式撰寫者和掃描器製造人員針對每個應用程式裝置組合自訂其應用程式或驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-118">This allows those different applications to talk to and interact with those different scanners without requiring the application writers and scanner manufactures to customize their application or drivers for each application-device combination.</span></span>

![<span data-ttu-id="8286e-119">圖形顯示在影像處理應用程式和裝置之間，以雙向層呈現的 wia 基本架構。</span><span class="sxs-lookup"><span data-stu-id="8286e-119">graphic showing the basic architecture of wia as a two-way layer between imaging applications and devices.</span></span> ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a><span data-ttu-id="8286e-120">Windows 映像收購2.0 的優點</span><span class="sxs-lookup"><span data-stu-id="8286e-120">Benefits of Windows Image Acquisition 2.0</span></span>

<span data-ttu-id="8286e-121">WIA 可提供應用程式開發人員、裝置製造商以及需要與映射處理硬體互動之掃描器使用者的優點。</span><span class="sxs-lookup"><span data-stu-id="8286e-121">WIA provides benefits to application developers, device manufacturers, and scanner users who need to interact with imaging hardware.</span></span>

### <a name="for-application-writers"></a><span data-ttu-id="8286e-122">針對應用程式寫入器</span><span class="sxs-lookup"><span data-stu-id="8286e-122">For Application Writers</span></span>

-   <span data-ttu-id="8286e-123">Windows 會執行 WIA 驅動程式的認證程式，因此 WIA 應用程式保證會與所有以 WIA 為基礎的掃描程式相容。</span><span class="sxs-lookup"><span data-stu-id="8286e-123">Windows runs a certification process for WIA drivers so WIA applications are guaranteed to be base-level compatible with all WIA-based scanners.</span></span>
-   <span data-ttu-id="8286e-124">Wia 驅動程式是在 WIA 服務進程中載入，因此可提供更穩定的驅動程式環境。</span><span class="sxs-lookup"><span data-stu-id="8286e-124">WIA drivers are loaded in the WIA service process, thus providing a more stable driver environment.</span></span>
-   <span data-ttu-id="8286e-125">您可以透過 WIA 子系統所支援的推送事件，從掃描器掃描按鈕起始應用程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-125">Applications can be initiated from the scanner scan button via push events supported by the WIA subsystem.</span></span>
-   <span data-ttu-id="8286e-126">WIA 包含所有驅動程式都可利用的預設分割篩選;如此一來，應用程式就不需要撰寫程式碼來進行多重區域掃描，例如將大量相片分散到平台掃描器。</span><span class="sxs-lookup"><span data-stu-id="8286e-126">The WIA includes a default segmentation filter that all drivers can take advantage of; this way, applications do not have to write code for multi-region scanning for purposes such as separating out a large number of photos spread over a flatbed scanner.</span></span>

### <a name="for-device-manufactures"></a><span data-ttu-id="8286e-127">針對裝置製造商</span><span class="sxs-lookup"><span data-stu-id="8286e-127">For Device Manufactures</span></span>

-   <span data-ttu-id="8286e-128">WIA 驅動程式認證程式可協助驅動程式開發人員建立其驅動程式符合 WIA 規範。</span><span class="sxs-lookup"><span data-stu-id="8286e-128">WIA driver certification process helps driver developers in establishing that their driver is WIA-compliant.</span></span>
-   <span data-ttu-id="8286e-129">WIA 驅動程式可利用內建的分割篩選器、影像處理篩選和錯誤處理常式（如果選擇這樣做）。</span><span class="sxs-lookup"><span data-stu-id="8286e-129">WIA drivers can take advantage of a built-in segmentation filter, image processing filter and error handler, if they choose to do so.</span></span>
-   <span data-ttu-id="8286e-130">以 WIA 為基礎的掃描器可以立即在 Windows 上使用 Windows 掃描應用程式（例如 Windows 傳真和掃描和油漆）來運作。</span><span class="sxs-lookup"><span data-stu-id="8286e-130">WIA-based scanners work right out of the box on Windows with Windows scanning applications such as Windows Fax and Scan and Paint.</span></span>
-   <span data-ttu-id="8286e-131">WIA 驅動程式提供更好的 Windows 整合，例如完整的裝置體驗。</span><span class="sxs-lookup"><span data-stu-id="8286e-131">WIA drivers offer better integration with Windows such as the full device experience.</span></span>
-   <span data-ttu-id="8286e-132">Windows Vista 版本包含一個 WSD WIA 類別驅動程式，可讓所有與 Web Service for 掃描器相容的裝置 (WS-掃描) 通訊協定，以在沒有任何額外的驅動程式或軟體的情況下使用 WIA 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-132">Windows Vista release includes a WSD-WIA class driver that enables all devices compliant with Web Services for Scanner (WS-Scan) protocol to work with WIA applications without any additional driver or software.</span></span>

### <a name="for-scanner-users"></a><span data-ttu-id="8286e-133">針對掃描器使用者</span><span class="sxs-lookup"><span data-stu-id="8286e-133">For Scanner Users</span></span>

-   <span data-ttu-id="8286e-134">您可以從 Windows 應用程式（例如 Windows 傳真和掃描和油漆）使用 WIA 型掃描器，而不需要任何額外的軟體。</span><span class="sxs-lookup"><span data-stu-id="8286e-134">WIA-based scanners can be used from Windows applications such Windows Fax and Scan and Paint without the need for any additional software.</span></span>
-   <span data-ttu-id="8286e-135">以 WIA 為基礎的應用程式和掃描器也可以利用 WIA 附加元件（例如分割篩選器）來處理掃描器上的一些圖片，並在不需要使用者介入的情況下，將它們全部掃描到個別檔案。</span><span class="sxs-lookup"><span data-stu-id="8286e-135">WIA-based applications and scanners can also take advantage of WIA add-ons such as the segmentation filter which enables such features as processing a number of pictures on the scanner and scanning them all to individual files without user intervention.</span></span>
-   <span data-ttu-id="8286e-136">WIA 型裝置提供與其他 Windows 功能（例如 Windows 7 的 Device Stage 功能）更好的整合。</span><span class="sxs-lookup"><span data-stu-id="8286e-136">WIA-based devices offers a much better integration with other Windows features such as the Device Stage feature for Windows 7.</span></span>
-   <span data-ttu-id="8286e-137">WIA 藉由隔離驅動程式和應用程式，提供更強大、穩定且可靠的掃描體驗。</span><span class="sxs-lookup"><span data-stu-id="8286e-137">WIA provides a more robust, stable and reliable scanning experience by isolating the driver and the application.</span></span>

## <a name="development-of-windows-image-acquisition"></a><span data-ttu-id="8286e-138">開發 Windows 映像</span><span class="sxs-lookup"><span data-stu-id="8286e-138">Development of Windows Image Acquisition</span></span>

<span data-ttu-id="8286e-139">Windows 2000 和 Windows 95 或更新版本中的映射架構是由低層級的硬體抽象概念、映射架構 (STI) ，以及一組高階的 Api （稱為 TWAIN）所組成。</span><span class="sxs-lookup"><span data-stu-id="8286e-139">The imaging architecture in Windows 2000 and Windows 95 or later consisted of a low-level hardware abstraction, Still Image Architecture (STI), and a high-level set of APIs known as TWAIN.</span></span> <span data-ttu-id="8286e-140">Windows XP 和 Windows Me 的 WIA 都是引進的。</span><span class="sxs-lookup"><span data-stu-id="8286e-140">In Windows XP and Windows Me WIA was introduced.</span></span> <span data-ttu-id="8286e-141">WIA 是以 STI 為基礎的映射架構，但不需要 TWAIN，雖然您仍然支援 TWAIN 和 WIA。</span><span class="sxs-lookup"><span data-stu-id="8286e-141">WIA is an imaging architecture that builds on STI and does not require TWAIN, although TWAIN is still supported alongside WIA.</span></span>

<span data-ttu-id="8286e-142">WIA 1.0 是在 Windows Me 和 Windows XP 中引進，並支援掃描器、數位攝影機和數位視訊設備。</span><span class="sxs-lookup"><span data-stu-id="8286e-142">WIA 1.0 was introduced in Windows Me and Windows XP and supports scanners, digital cameras and digital video equipment.</span></span> <span data-ttu-id="8286e-143">WIA 2.0 已與 Windows Vista 一起發行。</span><span class="sxs-lookup"><span data-stu-id="8286e-143">WIA 2.0 was released with Windows Vista.</span></span> <span data-ttu-id="8286e-144">WIA 2.0 的目標物件是掃描器，但繼續透過 wia 1.0 至 wia 服務所提供的 WIA 2.0 相容性層，提供舊版 WIA 1.0 應用程式和裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="8286e-144">WIA 2.0 is targeted towards scanners but continues to offer support for legacy WIA 1.0 applications and devices through a WIA 1.0 to WIA 2.0 compatibility layer provided by the WIA service.</span></span> <span data-ttu-id="8286e-145">不過，已從 Windows Vista 的 WIA 移除影片內容支援。</span><span class="sxs-lookup"><span data-stu-id="8286e-145">However, video content support was removed from WIA for Windows Vista.</span></span> <span data-ttu-id="8286e-146">我們建議 Windows 可攜式裝置 (WPD) API 用於數位攝影機和數位視訊設備。</span><span class="sxs-lookup"><span data-stu-id="8286e-146">We recommend Windows Portable Devices (WPD) API for digital cameras and digital video equipment in the future.</span></span> <span data-ttu-id="8286e-147">除了原生 WIA 2.0 設備磁碟機和映射應用程式，在 Windows Vista 和 Windows 7 上仍會直接支援 WIA 1.0 和 STI TWAIN 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-147">WIA 1.0 as well as STI TWAIN drivers are still supported directly on Windows Vista and Windows 7 alongside native WIA 2.0 device drivers and imaging applications.</span></span>

## <a name="overview-of-windows-image-acquisition"></a><span data-ttu-id="8286e-148">Windows 映像取得簡介</span><span class="sxs-lookup"><span data-stu-id="8286e-148">Overview of Windows Image Acquisition</span></span>

<span data-ttu-id="8286e-149">WIA 提供的架構可讓裝置為作業系統提供獨特的功能，並可讓映射應用程式叫用這些獨特的功能。</span><span class="sxs-lookup"><span data-stu-id="8286e-149">WIA provides a framework that allows a device to present its unique capabilities to the operating system and allows imaging applications to invoke those unique capabilities.</span></span>

<span data-ttu-id="8286e-150">WIA 平臺包含資料取得通訊協定、設備磁碟機模型和介面 (的 DDI) 、API 和專用的 WIA 服務。</span><span class="sxs-lookup"><span data-stu-id="8286e-150">The WIA platform includes a data acquisition protocol, a Device Driver Model and Interface (DDI), an API and a dedicated WIA service.</span></span> <span data-ttu-id="8286e-151">此平臺也包含一組內建的核心模式驅動程式，可支援在本機透過 USB、串列/平行、SCSI 和 FireWire 介面連線的映射裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8286e-151">The platform also includes a set of built-in kernel mode drivers that support communication with imaging devices locally connected through USB, serial/parallel, SCSI and FireWire interfaces.</span></span> <span data-ttu-id="8286e-152">WIA 子系統也包含透明相容性層，可讓 TWAIN 相容的應用程式採用並使用以 WIA 驅動程式為基礎的裝置。</span><span class="sxs-lookup"><span data-stu-id="8286e-152">The WIA subsystem also includes a transparent compatibility layer which allows TWAIN compatible applications to employ and use WIA-driver-based devices.</span></span>

<span data-ttu-id="8286e-153">您也可以透過隨附于 Windows Vista 的 WSD WIA 類別驅動程式，從 Windows Vista 和 Windows 7 上的 WIA 相容映射應用程式，使用支援裝置 (WSD) 通訊協定的網路連線映射裝置。</span><span class="sxs-lookup"><span data-stu-id="8286e-153">Network connected imaging devices that support Web Services for Devices (WSD) protocol can also be used from WIA-compliant imaging applications on Windows Vista and Windows 7 out of the box via a WSD-WIA class driver that shipped as part of Windows Vista.</span></span> <span data-ttu-id="8286e-154">類別驅動程式會將 WIA 呼叫轉換為 WSD 呼叫，反之亦然，並讓現有的 WIA 應用程式能在沒有任何額外驅動程式的情況下，使用以 WSD 為基礎的掃描器。</span><span class="sxs-lookup"><span data-stu-id="8286e-154">The class driver converts WIA calls to WSD calls and vice versa and makes already existing WIA applications work with WSD based scanners without any additional driver.</span></span>

<span data-ttu-id="8286e-155">WIA 驅動程式是由使用者介面所組成 (UI) 元件和核心驅動程式元件，載入至兩個不同的進程空間：應用程式空間中的 UI 和 WIA 服務空間中的驅動程式核心。</span><span class="sxs-lookup"><span data-stu-id="8286e-155">WIA drivers are made up of a user interface (UI) component and a core driver component, loaded into two different process spaces: UI in the application space and the driver core in the WIA service space.</span></span> <span data-ttu-id="8286e-156">此服務會在 Windows XP 的本機系統內容中執行，並在從 Windows Server 2003 和 Windows Vista 開始的本機服務內容中執行，以增強安全性免于發生錯誤或惡意的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-156">The service runs in Local System context in Windows XP and runs in Local Service context starting with Windows Server 2003 and Windows Vista for enhanced security against buggy or malicious drivers.</span></span>

![圖形顯示 wia 的架構，以及它如何以服務的方式運作。](images/wia-arch.png)

<span data-ttu-id="8286e-158">WIA API 集會提供下列支援，藉此將影像應用程式公開給仍能取得映射的硬體功能：</span><span class="sxs-lookup"><span data-stu-id="8286e-158">The WIA API set exposes imaging applications to still image acquisition hardware functionality by providing support for:</span></span>

-   <span data-ttu-id="8286e-159">列舉可用的映射取得裝置。</span><span class="sxs-lookup"><span data-stu-id="8286e-159">Enumeration of available image acquisition devices.</span></span>
-   <span data-ttu-id="8286e-160">同時建立多個裝置的連接。</span><span class="sxs-lookup"><span data-stu-id="8286e-160">Creating connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="8286e-161">以標準且可擴充的方式查詢裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="8286e-161">Querying properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="8286e-162">使用標準和高效能傳輸機制來取得裝置資料。</span><span class="sxs-lookup"><span data-stu-id="8286e-162">Acquiring device data by using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="8286e-163">維護資料傳輸之間的影像屬性。</span><span class="sxs-lookup"><span data-stu-id="8286e-163">Maintaining image properties across data transfers.</span></span>
-   <span data-ttu-id="8286e-164">裝置狀態和掃描事件處理的通知。</span><span class="sxs-lookup"><span data-stu-id="8286e-164">Notification of device status and scan event handling.</span></span>

<span data-ttu-id="8286e-165">Windows 將腳本支援新增至 WIA，方法是在2002中發行已併入 windows Vista 的 WIA Automation 程式庫做為 Windows 映像取得 (WIA) Automation 層，並繼續成為 Windows 7 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8286e-165">Windows added scripting support to WIA by releasing the WIA Automation Library in 2002 that was incorporated in Windows Vista as Windows Image Acquisition (WIA) Automation Layer and continues to be a part of Windows 7.</span></span> <span data-ttu-id="8286e-166">WIA Automation 程式庫為啟用自動化的應用程式開發環境和程式設計語言（例如 Microsoft Visual Basic 6.0、Active Server Pages (ASP) 、VBScript 和 C）提供端對端映射取得功能 \# 。</span><span class="sxs-lookup"><span data-stu-id="8286e-166">The WIA Automation Library provides end-to-end image acquisition capabilities to automation-enabled application development environments and programming languages such as Microsoft Visual Basic 6.0, Active Server Pages (ASP), VBScript and C\#.</span></span>

<span data-ttu-id="8286e-167">針對 Windows 7，WIA Api 提供額外的支援來補充已存在的推播掃描支援。</span><span class="sxs-lookup"><span data-stu-id="8286e-167">For Windows 7, WIA APIs have additional support to complement the already existing push-scanning support.</span></span>

-   <span data-ttu-id="8286e-168">自動設定裝置起始掃描裝置前端面板上掃描器設定的掃描參數。</span><span class="sxs-lookup"><span data-stu-id="8286e-168">Auto-configured device initiated scanning with scan parameters configured at the scanner on the device front panel.</span></span>
-   <span data-ttu-id="8286e-169">自動來源選取裝置起始的掃描。</span><span class="sxs-lookup"><span data-stu-id="8286e-169">Automatic source selection for device-initiated scan.</span></span>

## <a name="facts-about-windows-image-acquisition-20"></a><span data-ttu-id="8286e-170">Windows 映像取得2.0 的相關事實</span><span class="sxs-lookup"><span data-stu-id="8286e-170">Facts about Windows Image Acquisition 2.0</span></span>

-   <span data-ttu-id="8286e-171">WIA 2.0 中的資料傳輸機制是以資料流程為基礎。</span><span class="sxs-lookup"><span data-stu-id="8286e-171">The data transfer mechanism in WIA 2.0 is stream based.</span></span> <span data-ttu-id="8286e-172">資料流程抽象會移除不同傳輸類型之間的差異，也允許在裝置與應用程式之間交換相互同意的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8286e-172">The stream abstraction removes the distinction between different transfer types and also allows exchange of mutually agreed-upon metadata between device and application.</span></span>
-   <span data-ttu-id="8286e-173">WIA 2.0 子系統也包含基本的影像處理篩選器驅動程式附加元件，如果驅動程式選擇提供自訂的影像處理篩選器，則可選擇性地取代掃描器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8286e-173">WIA 2.0 subsystem also includes a basic image processing filter driver add-on that is optionally replaceable by the scanner driver, if the driver chooses to provide a customized image processing filter.</span></span> <span data-ttu-id="8286e-174">內建篩選器可讓您處理透過掃描器取得的影像。</span><span class="sxs-lookup"><span data-stu-id="8286e-174">The built-in filter enables post processing of images acquired through the scanner.</span></span> <span data-ttu-id="8286e-175">當調整亮度和對比等小型設定時，影像處理篩選也會啟用即時軟體預覽。</span><span class="sxs-lookup"><span data-stu-id="8286e-175">Image processing filter also enables live software previews when small settings such as brightness and contrast are adjusted.</span></span>
-   <span data-ttu-id="8286e-176">分割篩選是另一個方便使用的 WIA 元件，可由掃描器驅動程式以更自訂的篩選來取代。</span><span class="sxs-lookup"><span data-stu-id="8286e-176">The segmentation filter is another handy WIA component that can be replaced by a more customized filter by the scanner driver.</span></span> <span data-ttu-id="8286e-177">分割篩選可以用於多重區域掃描。</span><span class="sxs-lookup"><span data-stu-id="8286e-177">The segmentation filter can be used for multi-region scanning.</span></span> <span data-ttu-id="8286e-178">例如，多重區域掃描可讓應用程式在不需要使用者介入的情況下，自動偵測不同的掃描區域，例如識別掃描器平板上隨機拍攝的大量相片。</span><span class="sxs-lookup"><span data-stu-id="8286e-178">Multi-region scanning, as an example, allows an application to automatically detect different scan regions without any user intervention, such as identifying a bunch of photos lying randomly on the scanner flatbed.</span></span>
-   <span data-ttu-id="8286e-179">WIA 2.0 提供可取代/可延伸的錯誤處理常式，可正常處理並可能從軟體、硬體和設定錯誤和延遲中復原。</span><span class="sxs-lookup"><span data-stu-id="8286e-179">WIA 2.0 provides a replaceable/extensible error handler to gracefully handle, and possibly recover from, software, hardware and configuration errors and delays.</span></span> <span data-ttu-id="8286e-180">錯誤處理常式是另一個 WIA 元件，可由掃描器驅動程式以更自訂的版本取代。</span><span class="sxs-lookup"><span data-stu-id="8286e-180">The error handler is another WIA component that can be replaced with a more customized version by the scanner driver.</span></span> <span data-ttu-id="8286e-181">此延伸模組會在資料的取得期間提供狀態和錯誤訊息，例如「燈泡準備」、「說明開啟」、「紙紙」等等。</span><span class="sxs-lookup"><span data-stu-id="8286e-181">This extension provides status and error messages during data acquisitions such as "Lamp warming up," "Cover open," "Paper jam," and so on.</span></span> <span data-ttu-id="8286e-182">此延伸模組也可讓您更清楚支援「取消作業」。</span><span class="sxs-lookup"><span data-stu-id="8286e-182">This extension also allows cleaner support for "Cancel operations."</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8286e-183">開發人員讀者</span><span class="sxs-lookup"><span data-stu-id="8286e-183">Developer Audience</span></span>

<span data-ttu-id="8286e-184">WIA API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="8286e-184">The WIA API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="8286e-185">需要熟悉 Windows GUI 和元件物件模型 (COM) 介面。</span><span class="sxs-lookup"><span data-stu-id="8286e-185">Familiarity with the Windows  GUI and Component Object Model (COM) interfaces is required.</span></span>

<span data-ttu-id="8286e-186">針對熟悉 Microsoft Visual Basic 6.0、Active Server Pages (ASP) 或腳本處理的開發人員，WIA 提供適用于 Windows XP Service Pack 1 (SP1) 或更新版本的自動化層，其建立依據和簡化 C/c + + 所提供之基礎的存取。</span><span class="sxs-lookup"><span data-stu-id="8286e-186">For developers familiar with Microsoft Visual Basic 6.0, Active Server Pages (ASP), or scripting, WIA provides an automation layer for Windows XP Service Pack 1 (SP1) or later that builds upon and simplifies access to the foundation provided by C/C++.</span></span> <span data-ttu-id="8286e-187">如需自動化層的詳細資訊，請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="8286e-187">For information about the automation layer, see [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

> [!Note]  
> <span data-ttu-id="8286e-188">WIA 自動化層取代 Windows 映像取得 (WIA) 1.0 腳本。</span><span class="sxs-lookup"><span data-stu-id="8286e-188">The WIA Automation Layer supersedes Windows Image Acquisition (WIA) 1.0 scripting.</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="8286e-189">執行階段需求</span><span class="sxs-lookup"><span data-stu-id="8286e-189">Run-Time Requirements</span></span>

<span data-ttu-id="8286e-190">使用 WIA API 的應用程式需要 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8286e-190">Applications that use the WIA API require Windows XP or later.</span></span>

## <a name="wia-topics"></a><span data-ttu-id="8286e-191">WIA 主題</span><span class="sxs-lookup"><span data-stu-id="8286e-191">WIA Topics</span></span>

<span data-ttu-id="8286e-192">WIA 主題的組織方式如下表所示。</span><span class="sxs-lookup"><span data-stu-id="8286e-192">The WIA topics are organized as shown in the following table.</span></span>



|                                                                                                                              |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8286e-193">關於 Windows 映像取得</span><span class="sxs-lookup"><span data-stu-id="8286e-193">About Windows Image Acquisition</span></span>](-wia-about-windows-image-acquisition.md)                                                  | <span data-ttu-id="8286e-194">關於 WIA 的一般資訊</span><span class="sxs-lookup"><span data-stu-id="8286e-194">General information about WIA</span></span>                                                                     |
| [<span data-ttu-id="8286e-195">Windows 映像取得驅動程式</span><span class="sxs-lookup"><span data-stu-id="8286e-195">Windows Image Acquisition Drivers</span></span>](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | <span data-ttu-id="8286e-196">WIA 驅動程式開發</span><span class="sxs-lookup"><span data-stu-id="8286e-196">WIA driver development</span></span>                                                                            |
| [<span data-ttu-id="8286e-197">Windows 映像取得自動化層</span><span class="sxs-lookup"><span data-stu-id="8286e-197">Windows Image Acquisition Automation Layer</span></span>](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | <span data-ttu-id="8286e-198">WIA 自動化層</span><span class="sxs-lookup"><span data-stu-id="8286e-198">WIA Automation Layer</span></span>                                                                              |
| [<span data-ttu-id="8286e-199">WIA 教學課程</span><span class="sxs-lookup"><span data-stu-id="8286e-199">WIA Tutorial</span></span>](-wia-wia-tutorial.md)                                                                                        | <span data-ttu-id="8286e-200">軟體發展工具組中包含的程式碼逐步解說 (SDK) ，其著重于特定工作</span><span class="sxs-lookup"><span data-stu-id="8286e-200">Walkthrough of code included in the software development kit (SDK) that focuses on specific tasks</span></span> |
| [<span data-ttu-id="8286e-201">參考</span><span class="sxs-lookup"><span data-stu-id="8286e-201">Reference</span></span>](-wia-reference.md)                                                                                              | <span data-ttu-id="8286e-202">有關在 C/c + + 和腳本中使用的 WIA 介面、方法、物件和資料類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="8286e-202">Information on WIA interfaces, methods, objects, and data types used in C/C++ and scripting.</span></span>      |



 

 

 
