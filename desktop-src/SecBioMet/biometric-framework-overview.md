---
title: 生物特徵辨識架構總覽
description: 生物識別單元的原生支援會併入 Windows 中。
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463444"
---
# <a name="biometric-framework-overview"></a><span data-ttu-id="96464-103">生物特徵辨識架構總覽</span><span class="sxs-lookup"><span data-stu-id="96464-103">Biometric Framework overview</span></span>

<span data-ttu-id="96464-104">每個人都有唯一的特性可用於識別。</span><span class="sxs-lookup"><span data-stu-id="96464-104">Every individual has unique characteristics that can be used for identification.</span></span> <span data-ttu-id="96464-105">這些特性通常是實體的，而且包含指紋等特性，但也可以包含行為特性，例如 gait 和輸入節奏。</span><span class="sxs-lookup"><span data-stu-id="96464-105">Typically these characteristics are physical and include traits such as fingerprints, but they can also include behavioral traits such as gait and typing rhythm.</span></span> <span data-ttu-id="96464-106">生物特徵辨識詞彙包含這兩種意義。</span><span class="sxs-lookup"><span data-stu-id="96464-106">The term biometrics encompasses both meanings.</span></span> <span data-ttu-id="96464-107">生物特徵辨識資訊逐漸取代密碼以識別和驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="96464-107">Biometric information is increasingly replacing passwords to identify and verify users.</span></span> <span data-ttu-id="96464-108">這對使用者和系統管理員來說更安全，而且通常更方便。</span><span class="sxs-lookup"><span data-stu-id="96464-108">It is more secure and often more convenient for both user and administrator.</span></span>

<span data-ttu-id="96464-109">感應器可用來捕捉生物特徵辨識資訊。</span><span class="sxs-lookup"><span data-stu-id="96464-109">Sensors are used to capture biometric information.</span></span> <span data-ttu-id="96464-110">感應器會將此資訊視為生物特徵辨識範例。</span><span class="sxs-lookup"><span data-stu-id="96464-110">The information is captured by the sensor as a biometric sample.</span></span> <span data-ttu-id="96464-111">單一範例包含的資料代表一個個人的單一生物特徵辨識特性。</span><span class="sxs-lookup"><span data-stu-id="96464-111">A single sample contains data that represents a single biometric characteristic for one individual.</span></span> <span data-ttu-id="96464-112">建立生物特徵辨識範本的平均是多個範例，且範本會安全地儲存。</span><span class="sxs-lookup"><span data-stu-id="96464-112">Multiple samples are averaged to create a biometric template, and the template is securely stored.</span></span> <span data-ttu-id="96464-113">之後，來自未知使用者的範例會與已儲存的範本進行比較，以建立及驗證使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="96464-113">Later, a sample from an unknown user is compared to the stored templates to establish and verify user identity.</span></span> <span data-ttu-id="96464-114">Windows 生物識別服務（屬於 Windows 生物特徵辨識架構 (WBF) 的一部分）提供下列功能。</span><span class="sxs-lookup"><span data-stu-id="96464-114">The Windows Biometric service, part of the Windows Biometric Framework (WBF), provides the following functionality.</span></span> <span data-ttu-id="96464-115">您可以使用 Windows 生物特徵辨識架構 API 來利用此功能。</span><span class="sxs-lookup"><span data-stu-id="96464-115">You can use the Windows Biometric Framework API to leverage this functionality.</span></span>

-   <span data-ttu-id="96464-116">擷取生物識別樣本並用來建立範本。</span><span class="sxs-lookup"><span data-stu-id="96464-116">Captures biometric samples and uses them to create a template.</span></span>
-   <span data-ttu-id="96464-117">安全地儲存和取出生物特徵辨識範本。</span><span class="sxs-lookup"><span data-stu-id="96464-117">Securely saves and retrieves biometric templates.</span></span>
-   <span data-ttu-id="96464-118">將每個範本對應至唯一識別碼，例如 GUID 或 SID。</span><span class="sxs-lookup"><span data-stu-id="96464-118">Maps each template to a unique identifier such as a GUID or SID.</span></span>

<span data-ttu-id="96464-119">您也可以使用此 API 來延伸架構，以及建立生物特徵辨識感應器介面卡、相符引擎和儲存體元件。</span><span class="sxs-lookup"><span data-stu-id="96464-119">You can also use this API to extend the framework and create biometric sensor adapters, matching engines, and storage components.</span></span> <span data-ttu-id="96464-120">如需建立感應器介面卡、相符引擎和儲存元件的詳細資訊，請參閱 [建立介面卡外掛程式](creating-adapter-plug-ins.md)。</span><span class="sxs-lookup"><span data-stu-id="96464-120">For more information about creating sensor adapters, matching engines, and storage components, see [Creating Adapter Plug-ins](creating-adapter-plug-ins.md).</span></span>

## <a name="core-platform-components"></a><span data-ttu-id="96464-121">核心平臺元件</span><span class="sxs-lookup"><span data-stu-id="96464-121">Core platform components</span></span>

### <a name="windows-biometric-driver-interface-wbdi"></a><span data-ttu-id="96464-122">Windows 生物識別驅動程式介面 (WBDI)</span><span class="sxs-lookup"><span data-stu-id="96464-122">Windows Biometric Driver Interface (WBDI)</span></span>

<span data-ttu-id="96464-123">WBDI 是一種程式設計介面，可供生物特徵辨識驅動程式用來透過 Windows 生物特徵辨識服務 (WBS) 公開生物特徵辨識裝置。</span><span class="sxs-lookup"><span data-stu-id="96464-123">WBDI is a programming interface that a biometric driver can use to expose the biometric device through the Windows Biometric Service (WBS).</span></span> <span data-ttu-id="96464-124">您可以使用任何支援的驅動程式技術來執行 WBDI 驅動程式，包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="96464-124">You can implement a WBDI driver by using any supported driver technology, including the following.</span></span> <span data-ttu-id="96464-125">不過，我們建議您盡可能使用 UMDF 來改善驅動程式品質和系統穩定性。</span><span class="sxs-lookup"><span data-stu-id="96464-125">We recommend, however, that you use UMDF when possible to improve driver quality and system stability.</span></span>

-   <span data-ttu-id="96464-126">使用者模式驅動程式架構 (的 UMDF) </span><span class="sxs-lookup"><span data-stu-id="96464-126">User Mode Driver Framework (UMDF)</span></span>
-   <span data-ttu-id="96464-127">核心模式驅動程式架構 (KMDF) </span><span class="sxs-lookup"><span data-stu-id="96464-127">Kernel Mode Driver Framework (KMDF)</span></span>
-   <span data-ttu-id="96464-128">Windows Driver Model (WDM) </span><span class="sxs-lookup"><span data-stu-id="96464-128">Windows Driver Model (WDM)</span></span>

<span data-ttu-id="96464-129">WBDI 生物特徵辨識驅動程式也必須支援 WBDI 驅動程式介面 GUID 和所有必要的 i/o 控制項， (IOCTLs) 。</span><span class="sxs-lookup"><span data-stu-id="96464-129">A WBDI biometric driver must also support the WBDI driver interface GUID and all mandatory I/O controls (IOCTLs).</span></span> <span data-ttu-id="96464-130">驅動程式開發人員應該複習 Windows 驅動程式套件 (WDK) 的檔和範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="96464-130">Driver developers should review the documentation and sample code in the Windows Driver Kit (WDK).</span></span>

### <a name="windows-biometric-service-wbs"></a><span data-ttu-id="96464-131">Windows 生物特徵辨識服務 (WBS) </span><span class="sxs-lookup"><span data-stu-id="96464-131">Windows Biometric Service (WBS)</span></span>

<span data-ttu-id="96464-132">Windows 生物特徵辨識服務會管理已安裝的生物特徵辨識驅動程式，並支援 Windows 生物特徵辨識架構 API 來提供用戶端應用程式的裝置存取權。</span><span class="sxs-lookup"><span data-stu-id="96464-132">The Windows Biometric Service manages installed biometric drivers and supports the Windows Biometric Framework API to provide device access to client applications.</span></span> <span data-ttu-id="96464-133">WBS 會執行下列功能：</span><span class="sxs-lookup"><span data-stu-id="96464-133">WBS performs the following functions:</span></span>

-   <span data-ttu-id="96464-134">它會將用戶端應用程式與生物特徵辨識資料分開，以保護使用者的機密性。</span><span class="sxs-lookup"><span data-stu-id="96464-134">It protects user confidentiality by separating client applications from biometric data.</span></span>
-   <span data-ttu-id="96464-135">它會要求應用程式使用唯一識別碼來取得資料的存取權，以保護來自無許可權用戶端應用程式的生物特徵辨識資料。</span><span class="sxs-lookup"><span data-stu-id="96464-135">It protects biometric data from unprivileged client applications by requiring that applications gain access to data by using unique identifiers.</span></span>
-   <span data-ttu-id="96464-136">它會使用稱為 [生物識別單位](/previous-versions//dd401512(v=vs.85)) 的軟體元件，透過標準化介面公開特定生物特徵辨識裝置的功能。</span><span class="sxs-lookup"><span data-stu-id="96464-136">It uses a software component called a [Biometric Unit](/previous-versions//dd401512(v=vs.85)) to expose the capabilities of a particular biometric device through a standardized interface.</span></span>
-   <span data-ttu-id="96464-137">它會藉由將生物識別單位組成系統、私人或未指派的 [感應器](sensor-pools.md)集區來管理它們。</span><span class="sxs-lookup"><span data-stu-id="96464-137">It manages biometric units by grouping them into system, private, or unassigned [Sensor Pools](sensor-pools.md).</span></span>
-   <span data-ttu-id="96464-138">它支援針對缺乏上架處理或儲存功能的實體裝置使用生物識別單位 [介面卡](/previous-versions//dd401508(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="96464-138">It supports the use of biometric unit [Adapters](/previous-versions//dd401508(v=vs.85)) for physical devices that lack onboard processing or storage capabilities.</span></span>

### <a name="windows-biometric-framework-api"></a><span data-ttu-id="96464-139">Windows 生物特徵辨識架構 API</span><span class="sxs-lookup"><span data-stu-id="96464-139">Windows Biometric Framework API</span></span>

<span data-ttu-id="96464-140">Windows 生物特徵辨識架構 API 可讓您建立可與 Windows 生物特徵辨識服務互動的用戶端應用程式，以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="96464-140">The Windows Biometric Framework API enables you to create client applications that can interact with the Windows Biometric Service to perform the following actions:</span></span>

-   <span data-ttu-id="96464-141">識別並驗證使用者。</span><span class="sxs-lookup"><span data-stu-id="96464-141">Identify and verify users.</span></span>
-   <span data-ttu-id="96464-142">找出生物特徵辨識裝置並查詢其功能。</span><span class="sxs-lookup"><span data-stu-id="96464-142">Locate biometric devices and query their capabilities.</span></span>
-   <span data-ttu-id="96464-143">管理會話和監視事件。</span><span class="sxs-lookup"><span data-stu-id="96464-143">Manage sessions and monitor events.</span></span>

## <a name="user-experience-components"></a><span data-ttu-id="96464-144">使用者體驗元件</span><span class="sxs-lookup"><span data-stu-id="96464-144">User Experience Components</span></span>

### <a name="discovery-points"></a><span data-ttu-id="96464-145">探索點</span><span class="sxs-lookup"><span data-stu-id="96464-145">Discovery Points</span></span>

<span data-ttu-id="96464-146">終端使用者可以透過下列任何方式找出生物識別單元：</span><span class="sxs-lookup"><span data-stu-id="96464-146">End users can locate biometric devices by any of the following means:</span></span>

-   <span data-ttu-id="96464-147">在 [開始搜尋] 文字方塊中輸入生物特徵辨識、指紋、臉部或其他相關片語，以啟動 [生物特徵辨識裝置] 控制台。</span><span class="sxs-lookup"><span data-stu-id="96464-147">Typing the words biometrics, fingerprint, face, or other related phrases into the Start Search text box to start the biometric devices control panel.</span></span> <span data-ttu-id="96464-148">生物特徵辨識的結果清單可包含 Windows 10 映射上的下列專案。</span><span class="sxs-lookup"><span data-stu-id="96464-148">The results list for biometrics can contain items such as the following on a Windows 10 image.</span></span>
    -   <span data-ttu-id="96464-149">安裝指紋登入</span><span class="sxs-lookup"><span data-stu-id="96464-149">Setup fingerprint sign-in</span></span>
    -   <span data-ttu-id="96464-150">設定臉部登入</span><span class="sxs-lookup"><span data-stu-id="96464-150">Setup face sign-in</span></span>

### <a name="supported-scenarios"></a><span data-ttu-id="96464-151">支援的案例</span><span class="sxs-lookup"><span data-stu-id="96464-151">Supported Scenarios</span></span>

<span data-ttu-id="96464-152">以下是支援的案例：</span><span class="sxs-lookup"><span data-stu-id="96464-152">The following scenarios are supported:</span></span>

-   <span data-ttu-id="96464-153">使用者可以使用指紋辨識器或焦點在臉部上的 IR 攝影機登入本機電腦、工作組或網域。</span><span class="sxs-lookup"><span data-stu-id="96464-153">Users can log on to a local computer, a workgroup, or to a domain by using a fingerprint reader, or IR camera focused on the face.</span></span>
-   <span data-ttu-id="96464-154">具有系統管理許可權的使用者可以使用指紋或臉部 (UAC) 來提升應用程式的使用者帳戶控制。</span><span class="sxs-lookup"><span data-stu-id="96464-154">A user with administrative privileges can elevate applications through User Account Control (UAC) by using a fingerprint or face.</span></span>

## <a name="management-components"></a><span data-ttu-id="96464-155">管理元件</span><span class="sxs-lookup"><span data-stu-id="96464-155">Management components</span></span>

<span data-ttu-id="96464-156">您可以使用群組原則或行動裝置管理 (MDM) 來管理生物識別系統。</span><span class="sxs-lookup"><span data-stu-id="96464-156">A biometric system can be managed using Group Policy or mobile device management (MDM).</span></span>

### <a name="biometric-system-management"></a><span data-ttu-id="96464-157">生物識別系統管理</span><span class="sxs-lookup"><span data-stu-id="96464-157">Biometric System Management</span></span>

<span data-ttu-id="96464-158">您可以使用群組原則或 MDM 來管理生物特徵辨識功能。</span><span class="sxs-lookup"><span data-stu-id="96464-158">You can manage biometric capabilities using Group Policy or MDM.</span></span> <span data-ttu-id="96464-159">群組原則可以進一步用來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="96464-159">Group Policy can further be used to perform the following actions:</span></span>

-   <span data-ttu-id="96464-160">指定快速切換使用者的超時期間（如果是由 ISV 所執行的話）。</span><span class="sxs-lookup"><span data-stu-id="96464-160">Specify the timeout period for fast user switching, if implemented by the ISV.</span></span>
-   <span data-ttu-id="96464-161">防止生物識別單元安裝。</span><span class="sxs-lookup"><span data-stu-id="96464-161">Prevent biometric device installation.</span></span>
-   <span data-ttu-id="96464-162">強制移除生物特徵辨識裝置的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="96464-162">Force the removal of drivers for biometric devices.</span></span>
-   <span data-ttu-id="96464-163">停用生物識別服務。</span><span class="sxs-lookup"><span data-stu-id="96464-163">Disable the biometric service.</span></span>

 

 