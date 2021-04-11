---
description: WMI 可透過 WMI 提供者取得可管理的 Windows 物件相關資料。
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: 將資料提供給 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691519"
---
# <a name="providing-data-to-wmi"></a><span data-ttu-id="cd0c9-103">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="cd0c9-103">Providing Data to WMI</span></span>

<span data-ttu-id="cd0c9-104">WMI 可透過 WMI [*提供者*](gloss-p.md)取得可管理的 Windows 物件相關資料。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-104">WMI makes data about Windows manageable objects available through WMI [*providers*](gloss-p.md).</span></span> <span data-ttu-id="cd0c9-105">提供者會從系統元件（例如，處理常式）或已檢測的應用程式（例如 SNMP 或 IIS）抓取資料，並透過 WMI 將該資料傳遞至管理應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-105">A provider retrieves data from a system component, such as a process, or an instrumented application, such as SNMP or IIS, and passes that data through WMI to a management application.</span></span> <span data-ttu-id="cd0c9-106">例如，當應用程式或腳本使用 WMI [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process) 類別來要求處理資訊時，會透過預先安裝的提供者動態取得資料。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-106">For example, when an application or script requests process information using the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class, the data is obtained dynamically through a preinstalled provider.</span></span>

<span data-ttu-id="cd0c9-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="cd0c9-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="cd0c9-108">為可管理的物件建立模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-108">Creating a Model for a Manageable Object</span></span>](#creating-a-model-for-a-manageable-object)
-   [<span data-ttu-id="cd0c9-109">針對可管理的物件執行模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-109">Implementing a Model for a Manageable Object</span></span>](#implementing-a-model-for-a-manageable-object)
-   [<span data-ttu-id="cd0c9-110">判斷要執行的提供者類型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-110">Determining a Provider Type to Implement</span></span>](#determining-a-provider-type-to-implement)
-   [<span data-ttu-id="cd0c9-111">判斷提供者的裝載 (實) 模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-111">Determining a Hosting (Implementation) Model for a Provider</span></span>](#determining-a-hosting-implementation-model-for-a-provider)
-   [<span data-ttu-id="cd0c9-112">執行提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-112">Implementing a Provider</span></span>](#implementing-a-provider)
-   [<span data-ttu-id="cd0c9-113">向 WMI 和系統註冊提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-113">Registering a Provider with WMI and the System</span></span>](#registering-a-provider-with-wmi-and-the-system)
-   [<span data-ttu-id="cd0c9-114">測試提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-114">Testing a Provider</span></span>](#testing-a-provider)
-   [<span data-ttu-id="cd0c9-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd0c9-115">Related topics</span></span>](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a><span data-ttu-id="cd0c9-116">為可管理的物件建立模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-116">Creating a Model for a Manageable Object</span></span>

<span data-ttu-id="cd0c9-117">開發提供者之前，請先建立資料模型來代表可透過 WMI 公開的可管理物件。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-117">Before developing a provider, create a data model to represent the manageable object to be exposed through WMI.</span></span> <span data-ttu-id="cd0c9-118">您可以規劃提供者將公開的資料物件。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-118">You plan which data objects your provider will expose.</span></span> <span data-ttu-id="cd0c9-119">例如，如果您打算管理桌面背景的螢幕解析度，就必須決定如何在 [*受控物件格式 (MOF)*](gloss-m.md) 檔中建立桌面模型。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-119">For example, if you plan to manage the screen resolution of the desktop background, you must decide how to model the Desktop in a [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

<span data-ttu-id="cd0c9-120">若要建立有用的模型：</span><span class="sxs-lookup"><span data-stu-id="cd0c9-120">To create a useful model:</span></span>

-   <span data-ttu-id="cd0c9-121">判斷真實世界的案例，並為客戶可能想要讀取和更新的資訊建立模型 (例如，變更每個可管理物件的背景影像) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-121">Determine real world scenarios and model the information a customer may want to read and update (for example, changing the background image) for each manageable object.</span></span> <span data-ttu-id="cd0c9-122">這些是您的類別屬性。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-122">These are your class properties.</span></span>
-   <span data-ttu-id="cd0c9-123">判斷客戶可能想要對每個可管理的物件執行何種動作。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-123">Determine which kind of actions a customer may want to perform with each manageable object.</span></span> <span data-ttu-id="cd0c9-124">這些都是您的方法。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-124">These are your methods.</span></span>

## <a name="implementing-a-model-for-a-manageable-object"></a><span data-ttu-id="cd0c9-125">針對可管理的物件執行模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-125">Implementing a Model for a Manageable Object</span></span>

<span data-ttu-id="cd0c9-126">若要針對可管理的物件執行模型，請建立一個 MOF 檔案，其中包含代表每個物件的 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-126">To implement a model for manageable objects, create a MOF file containing a WMI class that represents each object.</span></span> <span data-ttu-id="cd0c9-127">如需建立 MOF 檔案以定義 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-127">For more information about creating a MOF file to define WMI classes, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span> <span data-ttu-id="cd0c9-128">註冊提供者及其類別通常會包含在 MOF 檔案中，雖然您可以使用 [COM API](com-api-for-wmi.md) 來建立類別和方法。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-128">The registration of the provider and its classes are usually included in the MOF file, although it is possible to use the [COM API](com-api-for-wmi.md) to create classes and methods.</span></span> <span data-ttu-id="cd0c9-129">如需詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-129">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="cd0c9-130">若要確保在 WMI 失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式 (MOF)*](gloss-m.md)檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-130">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="cd0c9-131">建立 MOF 檔案之後，請使用 [**Mofcomp.exe**](mofcomp.md) 工具進行編譯。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-131">After you create the MOF file, compile it using the [**Mofcomp.exe**](mofcomp.md) tool.</span></span> <span data-ttu-id="cd0c9-132">這會通知您 MOF 檔案中的錯誤，並將 MOF 檔案中定義的 WMI 類別新增至 [*wmi 儲存*](gloss-w.md) 機制，讓提供者可以使用此類別。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-132">This notifies you of errors in your MOF file, and adds the WMI class defined in the MOF file to the [*WMI repository*](gloss-w.md) so that the class can be used by a provider.</span></span>

## <a name="determining-a-provider-type-to-implement"></a><span data-ttu-id="cd0c9-133">判斷要執行的提供者類型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-133">Determining a Provider Type to Implement</span></span>

<span data-ttu-id="cd0c9-134">WMI 支援特定數目的提供者類型，可決定提供者所支援之資訊和作業的本質。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-134">WMI supports a certain number of provider types, which determines the nature of the information delivered and operations supported by the providers.</span></span>

<span data-ttu-id="cd0c9-135">提供者類型為：</span><span class="sxs-lookup"><span data-stu-id="cd0c9-135">The provider types are:</span></span>

-   [<span data-ttu-id="cd0c9-136">*執行個體提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-136">*Instance provider*</span></span>](gloss-i.md)
-   [<span data-ttu-id="cd0c9-137">*方法提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-137">*Method provider*</span></span>](gloss-m.md)
-   [<span data-ttu-id="cd0c9-138">*屬性提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-138">*Property provider*</span></span>](gloss-p.md)
-   <span data-ttu-id="cd0c9-139">類別提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-139">Class provider</span></span>
-   [<span data-ttu-id="cd0c9-140">*事件提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-140">*Event provider*</span></span>](gloss-e.md)
-   [<span data-ttu-id="cd0c9-141">*事件取用者提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-141">*Event consumer provider*</span></span>](gloss-e.md)
-   [<span data-ttu-id="cd0c9-142">*關聯提供者*</span><span class="sxs-lookup"><span data-stu-id="cd0c9-142">*Association provider*</span></span>](gloss-a.md)

<span data-ttu-id="cd0c9-143">大部分的提供者都是執行個體提供者和方法提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-143">The vast majority of providers are instance providers and method providers.</span></span> <span data-ttu-id="cd0c9-144">執行個體提供者是最常見的提供者，它會提供指定類別的實例。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-144">An instance provider is the most common provider, and it supplies the instances of a given class.</span></span> <span data-ttu-id="cd0c9-145">方法提供者會執行一個或多個類別的方法。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-145">A method provider implements the methods of one or more classes.</span></span> <span data-ttu-id="cd0c9-146">如需提供者類型的詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-146">For more information about the types of providers, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a><span data-ttu-id="cd0c9-147">判斷提供者的裝載 (實) 模型</span><span class="sxs-lookup"><span data-stu-id="cd0c9-147">Determining a Hosting (Implementation) Model for a Provider</span></span>

<span data-ttu-id="cd0c9-148">WMI 提供者是實作為 COM 物件的二進位檔。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-148">WMI providers are binaries implemented as COM objects.</span></span> <span data-ttu-id="cd0c9-149">這表示每個提供者都有一個 DLL 檔案，可在特定進程和安全性內容中執行。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-149">This means that each provider has a DLL file which can be executed within a specific process and security context.</span></span> <span data-ttu-id="cd0c9-150">這是 WMI 所謂的 [*裝載模型*](gloss-h.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-150">This is what WMI refers to as the [*hosting model*](gloss-h.md).</span></span> <span data-ttu-id="cd0c9-151">WMI 提供各種不同的方式來主控提供者，但最常見的方法是使用結合的提供者模型 (在 NetworkServiceHost 安全性內容中) 的 WMI 進程下執行。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-151">WMI offers various ways to host providers, but the most common approach is to use the coupled provider model (running under the WMI process) in the NetworkServiceHost security context.</span></span> <span data-ttu-id="cd0c9-152">WMI 提供者可分類為結合或 [*分離*](gloss-d.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-152">A WMI provider can be classified as either coupled or [*decoupled*](gloss-d.md).</span></span>

<span data-ttu-id="cd0c9-153">「結合」或「分離」提供者會根據提供的 WMI （WMIPRVSE.EXE 程式），決定執行提供者所依據的主機進程。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-153">The term coupled or decoupled provider determines under which host process the provider is running with respect to the WMI provided WMIPRVSE.EXE process.</span></span> <span data-ttu-id="cd0c9-154">最佳做法是判斷提供者公開的管理資料，以及它所依賴的 API 或應用程式是否一律可在系統中使用。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-154">A best practice is to determine if the management data that the provider exposes and the API or application it relies on are always available in the system or not.</span></span> <span data-ttu-id="cd0c9-155">如果提供者所依賴的 API 或應用程式永遠可用 (在系統) 上執行，則提供者應該是結合的提供者，如果不是，則必須是低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-155">If the API or application the provider relies on is always available (running on the system), then the provider should be a coupled provider, if not, it must be a decoupled provider.</span></span> <span data-ttu-id="cd0c9-156">如需裝載模型的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-156">For more information about hosting models, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="cd0c9-157">如需有關建立結合提供者的詳細資訊，請參閱 [撰寫提供者以將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)，以及如需在應用程式中納入低耦合提供者的詳細資訊，請參閱 [在應用程式中併入提供者](incorporating-a-provider-in-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-157">For more information about creating a coupled provider, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md), and for information about incorporating a decoupled provider in an application, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="cd0c9-158">結合的提供者可以描述為同進程 (內建) 或跨進程的 (跨進程) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-158">Coupled providers can be described as in-process (in-proc) or out-of-process (out-of-proc).</span></span> <span data-ttu-id="cd0c9-159">當結合的提供者是內建提供者時，它會在共用 WMIPRVSE.EXE WMI 裝載進程下執行，並實作為 COM 的內部進程伺服器 ( .dll) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-159">When a coupled provider is an in-proc provider, it runs under a shared WMIPRVSE.EXE WMI hosting process and is implemented as a COM in-proc server (.dll).</span></span> <span data-ttu-id="cd0c9-160">當提供者是跨進程提供者時，它會在要求用戶端或事件時由 WMI 啟動，但會以分開進程的形式執行，並實作為可執行檔 ( .exe) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-160">When a provider is an out-of-proc provider, it is started by WMI on request of a client or event, but it runs as a separated process and is implemented as an executable (.exe).</span></span>

## <a name="implementing-a-provider"></a><span data-ttu-id="cd0c9-161">執行提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-161">Implementing a Provider</span></span>

<span data-ttu-id="cd0c9-162">您可以透過下列方式實作為提供者：</span><span class="sxs-lookup"><span data-stu-id="cd0c9-162">A provider can be implemented in the following ways:</span></span>

-   <span data-ttu-id="cd0c9-163">使用 Visual Studio 中的 ATL Wizard。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-163">Using the ATL Wizard in Visual Studio.</span></span>

    <span data-ttu-id="cd0c9-164">ATL Wizard 會產生可執行結合提供者的提供者程式碼。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-164">The ATL Wizard generates provider code that implements a coupled provider.</span></span> <span data-ttu-id="cd0c9-165">當您使用 ATL Wizard 時，可以指定要建立同進程 ( .dll) 或非進程 ( .exe) 提供者執行時間模型。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-165">While using the ATL Wizard, you can specify that you want to create an in-proc (.dll) or out-of-proc (.exe) provider run-time model.</span></span>

-   <span data-ttu-id="cd0c9-166">定義要包含提供者的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-166">Defining a COM object to contain your provider.</span></span>

    <span data-ttu-id="cd0c9-167">提供者程式碼是以 c + + 撰寫。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-167">The provider code is written in C++.</span></span> <span data-ttu-id="cd0c9-168">如需詳細資訊，請參閱 [撰寫提供者以將資料提供給 WMI](supplying-data-to-wmi-by-writing-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-168">For more information, see [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).</span></span>

-   <span data-ttu-id="cd0c9-169">使用 .NET Framework [**中的類別**](/previous-versions//hh872326(v=vs.85)) ，利用 managed 程式碼來建立提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-169">Using the classes in the [**Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) namespace in the .NET Framework to create a provider using managed code.</span></span> <span data-ttu-id="cd0c9-170">不再支援 (**系統. Management. Instrumentation** 命名空間。 ) </span><span class="sxs-lookup"><span data-stu-id="cd0c9-170">(The **System.Management.Instrumentation** namespace is no longer supported.)</span></span>

    <span data-ttu-id="cd0c9-171">此進程會建立低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-171">This process creates a decoupled provider.</span></span>

## <a name="registering-a-provider-with-wmi-and-the-system"></a><span data-ttu-id="cd0c9-172">向 WMI 和系統註冊提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-172">Registering a Provider with WMI and the System</span></span>

<span data-ttu-id="cd0c9-173">使用來自取用者的提供者之前，請務必向 WMI 系統和 Windows COM 子系統註冊該提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-173">Before using the provider from a consumer, it is important to register it with the WMI system and the Windows COM subsystem.</span></span>

<span data-ttu-id="cd0c9-174">MOF 檔案可以包含相同類別的多個提供者類型。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-174">A MOF file can contain multiple types of providers for the same classes.</span></span> <span data-ttu-id="cd0c9-175">相同的提供者名稱會註冊為，例如實例或方法提供者。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-175">The same provider name is registered as, for example, an instance or a method provider.</span></span> <span data-ttu-id="cd0c9-176">如需詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-176">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

## <a name="testing-a-provider"></a><span data-ttu-id="cd0c9-177">測試提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-177">Testing a Provider</span></span>

<span data-ttu-id="cd0c9-178">註冊提供者程式碼時，請務必使用不同取用者的提供者來適當測試提供者 (例如，腳本、.NET managed 程式碼和 c + + 取用者) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-178">When the provider code is registered, it is important to properly test the provider by using the provider from different consumers (for example, scripts, .NET managed code, and C++ consumers).</span></span>

<span data-ttu-id="cd0c9-179">執行下列工作以測試您的提供者：</span><span class="sxs-lookup"><span data-stu-id="cd0c9-179">Perform the following tasks to test your provider:</span></span>

-   <span data-ttu-id="cd0c9-180">藉由追蹤 [**MSFT \_ 的 wmiprovider \_ OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) 事件通知，確定您的提供者已正確載入。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-180">Ensure that your provider is loading properly by tracking the [**MSFT\_WmiProvider\_OperationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) event notifications.</span></span> <span data-ttu-id="cd0c9-181">這些事件會通知您有任何提供者載入失敗。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-181">These events will inform you about any provider load failures.</span></span> <span data-ttu-id="cd0c9-182">其他可能會有説明的疑難排解類別是 [**win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) 和 [**win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-182">Other troubleshooting classes that may be helpful are [**Win32\_ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) and [**Win32\_ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace).</span></span> <span data-ttu-id="cd0c9-183">如需疑難排解提供者的詳細資訊，請參閱 [偵錯工具](debugging-providers.md) 和 [提供者設定和疑難排解類別](provider-configuration-and-troubleshooting-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-183">For more information about troubleshooting providers, see [Debugging Providers](debugging-providers.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).</span></span>
-   <span data-ttu-id="cd0c9-184">如果提供者是實例或方法提供者，請務必逐一測試每一項提供者功能，以避免混淆您的程式碼邏輯。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-184">If the provider is an instance or method provider, ensure you test each provider capability one-by-one to avoid confusion in following your code logic.</span></span>
-   <span data-ttu-id="cd0c9-185">若為執行個體提供者，請建立用戶端應用程式或腳本，以叫用提供者的每個介面 (列舉、get、put 和 delete) 。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-185">For an instance provider, create a client application or script that invokes every interface of the provider (enumeration, get, put, and delete).</span></span> <span data-ttu-id="cd0c9-186">即使提供者不應執行任何作業，它也應該會傳回「不支援」的訊息。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-186">Even if the provider is not supposed to implement anything, it should return a "not supported" message.</span></span> <span data-ttu-id="cd0c9-187">您可以找到已在 [WMI 傳回碼](wmi-return-codes.md)中定義的傳回值。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-187">You can find the return values already defined in [WMI Return Codes](wmi-return-codes.md).</span></span>
-   <span data-ttu-id="cd0c9-188">為了確保所需的安全性內容如預期運作，請從非管理員的安全性內容叫用提供者支援的作業。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-188">To ensure that the desired security context is working as planned, invoke the provider supported operations from a nonadministrator security context.</span></span> <span data-ttu-id="cd0c9-189">提供者必須支援模擬。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-189">The provider must support impersonation.</span></span> <span data-ttu-id="cd0c9-190">如果缺少正確安全性認證的使用者嘗試更新資料，或執行執行方法的作業，則您的提供者應該使用適當的錯誤訊息來拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-190">If a user lacking the correct security credentials tries to update data or perform an operation that executes a method, your provider should deny access with the appropriate error message.</span></span>
-   <span data-ttu-id="cd0c9-191">如需提供者安全性的詳細資訊，請參閱 [保護您的提供者](securing-your-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cd0c9-191">For more information about provider security, see [Securing Your Provider](securing-your-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd0c9-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="cd0c9-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd0c9-193">開發 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-193">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-194">提供者裝載和安全性</span><span class="sxs-lookup"><span data-stu-id="cd0c9-194">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-195">藉由撰寫提供者，將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="cd0c9-195">Supplying Data to WMI by Writing a Provider</span></span>](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-196">將提供者併入應用程式中</span><span class="sxs-lookup"><span data-stu-id="cd0c9-196">Incorporating a Provider in an Application</span></span>](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-197">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-197">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-198">疑難排解 WMI 用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="cd0c9-198">Troubleshooting WMI Client Applications</span></span>](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-199">保護您的提供者</span><span class="sxs-lookup"><span data-stu-id="cd0c9-199">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="cd0c9-200">在64位平臺上取得和提供資料</span><span class="sxs-lookup"><span data-stu-id="cd0c9-200">Getting and Providing Data on a 64-bit Platform</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
