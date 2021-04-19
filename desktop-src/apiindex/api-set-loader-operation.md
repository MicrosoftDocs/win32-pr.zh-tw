---
description: 描述 Windows 10 如何使用載入器作業中的 API 集合。
title: API 集合載入器作業
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106975580"
---
# <a name="api-set-loader-operation"></a><span data-ttu-id="9efce-103">API 集合載入器作業</span><span class="sxs-lookup"><span data-stu-id="9efce-103">API set loader operation</span></span>

<span data-ttu-id="9efce-104">[API 集會](windows-apisets.md) 依賴程式庫載入器中的作業系統支援，以有效地將模組命名空間重新導向至程式庫系結程式。</span><span class="sxs-lookup"><span data-stu-id="9efce-104">[API sets](windows-apisets.md) rely on OS support in the library loader to effectively introduce a module namespace redirection into the library binding process.</span></span> <span data-ttu-id="9efce-105">程式庫載入器會使用 [API 集合約名稱](windows-apisets.md#api-set-contract-names) ，針對裝載適當的 API 集執行的目標主機二進位檔，執行其參考的執行時間重新導向。</span><span class="sxs-lookup"><span data-stu-id="9efce-105">The [API set contract name](windows-apisets.md#api-set-contract-names) is used by library loader to perform a runtime redirection of the reference to a target host binary that houses the appropriate implementation of the API set.</span></span>

<span data-ttu-id="9efce-106">當載入器在執行時間遇到對 API 集的相依性時，載入器會查閱映射中的設定資料，以識別 API 集的主機二進位檔。</span><span class="sxs-lookup"><span data-stu-id="9efce-106">When the loader encounters a dependency on an API set at run time, the loader consults configuration data in the image to identify the host binary for an API set.</span></span> <span data-ttu-id="9efce-107">這項設定資料稱為 **API 集架構**。</span><span class="sxs-lookup"><span data-stu-id="9efce-107">This configuration data is called the **API set schema**.</span></span> <span data-ttu-id="9efce-108">架構會組合為 OS 的屬性，而且 API 集合和二進位檔之間的對應可能會根據指定裝置中包含的二進位檔而有所不同。</span><span class="sxs-lookup"><span data-stu-id="9efce-108">The schema is assembled as a property of the OS, and the mapping between API sets and binaries may differ depending on which binaries are included in a given device.</span></span> <span data-ttu-id="9efce-109">架構可讓單一二進位檔中的匯入函式在不同的裝置上正確地路由傳送，即使二進位主機的模組名稱已重新命名或在不同的 Windows 裝置上完全重構亦同。</span><span class="sxs-lookup"><span data-stu-id="9efce-109">The schema enables an imported function in a single binary to be routed correctly on different devices, even if the module names of the binary host have been renamed or completely refactored on different Windows devices.</span></span>

<span data-ttu-id="9efce-110">Windows 10 支援兩種標準技術來取用和介面與 API 集合： **直接轉送** 和 **反向轉送**。</span><span class="sxs-lookup"><span data-stu-id="9efce-110">Windows 10 supports two standard techniques to consume and interface with API sets: **direct forwarding** and **reverse forwarding**.</span></span>

### <a name="direct-forwarding"></a><span data-ttu-id="9efce-111">直接轉送</span><span class="sxs-lookup"><span data-stu-id="9efce-111">Direct forwarding</span></span>

<span data-ttu-id="9efce-112">在此設定中，使用程式碼會直接匯入 API 集模組名稱。</span><span class="sxs-lookup"><span data-stu-id="9efce-112">In this configuration, the consuming code imports an API set module name directly.</span></span> <span data-ttu-id="9efce-113">這項匯入是在單一作業中解決，而且是最有效率的方法，最少的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9efce-113">This import is resolved in a single operation, and is the most efficient method with the least overhead.</span></span> <span data-ttu-id="9efce-114">就概念而言，此解析可能會指向不同 Windows 10 裝置上的不同二進位檔，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="9efce-114">Conceptually, this resolution may point to different binaries on different Windows 10 devices, as is shown in the following example:</span></span>

<span data-ttu-id="9efce-115">匯入的 API 集： **api-feature1-l1-1-0.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-115">Imported API set: **api-feature1-l1-1-0.dll**</span></span>
-  <span data-ttu-id="9efce-116">Windows 電腦-> **feature1.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-116">Windows PC -> **feature1.dll**</span></span>
-  <span data-ttu-id="9efce-117">HoloLens-> **feature1_holo.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-117">HoloLens -> **feature1_holo.dll**</span></span>
-  <span data-ttu-id="9efce-118">IoT-> **feature1_iot.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-118">IoT -> **feature1_iot.dll**</span></span>

<span data-ttu-id="9efce-119">因為對應會保存在自訂架構資料存放庫中，所以表示以 **.dll** 結尾的 API 集名稱不會直接參考磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="9efce-119">Because the mappings are kept in a custom schema data repository, it means that an API set name that ends with **.dll** does not directly refer to a file on disk.</span></span> <span data-ttu-id="9efce-120">API 集合名稱的 **.dll** 部分只是載入器所需的慣例。</span><span class="sxs-lookup"><span data-stu-id="9efce-120">The **.dll** part of the API set name is only a convention required by the loader.</span></span> <span data-ttu-id="9efce-121">API 集合名稱比較像是實體 DLL 檔案的別名或虛擬名稱。</span><span class="sxs-lookup"><span data-stu-id="9efce-121">The API set name is more like an alias or a virtual name for a physical DLL file.</span></span> <span data-ttu-id="9efce-122">這讓名稱可在整個 Windows 10 裝置的範圍內移植。</span><span class="sxs-lookup"><span data-stu-id="9efce-122">This makes the name portable across the entire range of Windows 10 devices.</span></span>

### <a name="reverse-forwarding"></a><span data-ttu-id="9efce-123">反向轉送</span><span class="sxs-lookup"><span data-stu-id="9efce-123">Reverse forwarding</span></span>

<span data-ttu-id="9efce-124">雖然 API 集合名稱會為跨裝置的模組提供穩定的命名空間，但將每個二進位檔轉換成這個新系統並不一定都可行。</span><span class="sxs-lookup"><span data-stu-id="9efce-124">While API set names provide a stable namespace for modules across devices, it is not always practical to convert every binary to this new system.</span></span> <span data-ttu-id="9efce-125">例如，應用程式可能已普遍使用多年，而重新編譯應用程式的二進位檔可能不可行。</span><span class="sxs-lookup"><span data-stu-id="9efce-125">For example, an application may have been in common use for many years, and recompiling the application's binaries may not be feasible.</span></span> <span data-ttu-id="9efce-126">此外，某些應用程式可能需要繼續在引進特定 API 集合之前建立的系統上執行。</span><span class="sxs-lookup"><span data-stu-id="9efce-126">Additionally, some applications may need to continue to run on systems built before specific API sets were introduced.</span></span>

<span data-ttu-id="9efce-127">為了滿足此層級的相容性，所有涵蓋 WIN32 API 介面子集的 Windows 10 裝置 *上都會提供* 轉寄站系統。</span><span class="sxs-lookup"><span data-stu-id="9efce-127">To accommodate this level of compatibility, a system of *forwarders* are provided on all Windows 10 devices that cover a subset of the Win32 API surface.</span></span> <span data-ttu-id="9efce-128">這些轉寄站使用在 Windows 電腦上引進的模組名稱，並利用 API 集系統來提供所有 Windows 10 裝置的相容性。</span><span class="sxs-lookup"><span data-stu-id="9efce-128">These forwarders use the module names that were introduced on Windows PCs, and leverage the API Set system to provide compatibility across all Windows 10 devices.</span></span>

<span data-ttu-id="9efce-129">載入器作業的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="9efce-129">The loader operation behaves like this:</span></span>

1.  <span data-ttu-id="9efce-130">在 Windows 電腦以外的裝置上，載入器會顯示在裝置上不存在的舊版 Windows 電腦模組名稱相依性。</span><span class="sxs-lookup"><span data-stu-id="9efce-130">On a device other than a Windows PC, the loader is presented a legacy Windows PC module name dependency that is not present on the device.</span></span>
2.  <span data-ttu-id="9efce-131">載入器會尋找此模組的 API 集合轉寄站，並將其載入記憶體。</span><span class="sxs-lookup"><span data-stu-id="9efce-131">The loader locates an API set forwarder for this module and loads it into memory.</span></span>
3.  <span data-ttu-id="9efce-132">轉寄站具有針對所呼叫之指定函式所設定的 API 對應。</span><span class="sxs-lookup"><span data-stu-id="9efce-132">The forwarder has a mapping for the API set for the given function being called.</span></span>
4.  <span data-ttu-id="9efce-133">載入器會為指定的裝置尋找適當的主機二進位檔。</span><span class="sxs-lookup"><span data-stu-id="9efce-133">The loader finds the proper host binary for the given device.</span></span>

<span data-ttu-id="9efce-134">就概念而言，對應看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="9efce-134">Conceptually, the mapping looks like:</span></span>

<span data-ttu-id="9efce-135">匯入的 DLL： **feature1.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-135">Imported DLL: **feature1.dll**</span></span>
- <span data-ttu-id="9efce-136">Windows 電腦-> **feature1.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-136">Windows PC -> **feature1.dll**</span></span>
- <span data-ttu-id="9efce-137">HoloLens-> **feature1.dll** 轉寄站-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-137">HoloLens -> **feature1.dll** forwarder -> **api-feature1-l1-1-0.dll** -> **feature1_holo.dll**</span></span>
- <span data-ttu-id="9efce-138">IoT > **feature1.dll** 轉寄站-> **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**</span><span class="sxs-lookup"><span data-stu-id="9efce-138">IoT -> **feature1.dll** forwarder -> **api-feature1-l1-1-0.dll** -> **feature1_iot.dll**</span></span>

<span data-ttu-id="9efce-139">最終結果的功能與 [直接轉送](#direct-forwarding)相同，但它會以最大化應用程式相容性的方式來完成。</span><span class="sxs-lookup"><span data-stu-id="9efce-139">The end result is functionally the same as [direct forwarding](#direct-forwarding), but it accomplishes it in a way that maximizes application compatibility.</span></span>

> [!NOTE]
> <span data-ttu-id="9efce-140">反向轉送僅提供 WIN32 API 介面子集的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="9efce-140">Reverse forwarding provides coverage only for a subset of the Win32 API surface.</span></span> <span data-ttu-id="9efce-141">它不允許以桌上出版 Windows 10 為目標的應用程式在所有 Windows 10 裝置上執行。</span><span class="sxs-lookup"><span data-stu-id="9efce-141">It does not allow applications that target desktop versions of Windows 10 to run on all Windows 10 devices.</span></span>
