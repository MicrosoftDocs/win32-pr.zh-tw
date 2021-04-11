---
description: 在 WMI 中註冊提供者實體執行的相關資訊。 預設會載入未設定 HostingModel 屬性的提供者，以便在 Wmiprvse.exe 進程中以 NetworkServiceHostOrSelfHost 的形式執行。
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945118"
---
# <a name="__win32provider-class"></a><span data-ttu-id="cea4d-104">\_\_Win32Provider 類別</span><span class="sxs-lookup"><span data-stu-id="cea4d-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="cea4d-105">**\_ \_ Win32Provider** 系統類別會在 WMI 中註冊提供者實體執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cea4d-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="cea4d-106">預設會載入未設定 **HostingModel** 屬性的提供者，以便在 Wmiprvse.exe 進程中以 **NetworkServiceHostOrSelfHost** 的形式執行。</span><span class="sxs-lookup"><span data-stu-id="cea4d-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="cea4d-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cea4d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cea4d-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="cea4d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea4d-109">語法</span><span class="sxs-lookup"><span data-stu-id="cea4d-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="cea4d-110">成員</span><span class="sxs-lookup"><span data-stu-id="cea4d-110">Members</span></span>

<span data-ttu-id="cea4d-111">**\_ \_ Win32Provider** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cea4d-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="cea4d-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cea4d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cea4d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="cea4d-113">Properties</span></span>

<span data-ttu-id="cea4d-114">**\_ \_ Win32Provider** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cea4d-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cea4d-115">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="cea4d-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-118">WMI 用來判斷是否要將高效能提供者載入至用戶端進程或 WMI 進程的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="cea4d-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="cea4d-119">如果提供者和用戶端都位於相同的電腦上，WMI 會使用 **ClientLoadableCLSID** 做為類別識別碼，將處理常式載入至用戶端。</span><span class="sxs-lookup"><span data-stu-id="cea4d-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="cea4d-120">當提供者和用戶端位於不同的電腦上時，WMI 會將提供者載入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="cea4d-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="cea4d-121">WMI 也會使用 **ClientLoadableCLSID** 來支援重新整理作業。</span><span class="sxs-lookup"><span data-stu-id="cea4d-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="cea4d-122">如需詳細資訊，請參閱 [註冊 High-Performance 提供者。](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="cea4d-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-123">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="cea4d-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-126">**GUID** ，表示提供者 COM 物件 (**CLSID**) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="cea4d-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="cea4d-127">這個 COM 物件必須包含 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="cea4d-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-128">**並行**</span><span class="sxs-lookup"><span data-stu-id="cea4d-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea4d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-131">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-132">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="cea4d-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-135">識別要啟動提供者的電腦。</span><span class="sxs-lookup"><span data-stu-id="cea4d-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="cea4d-136">如果提供者在本機電腦上執行，則為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="cea4d-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-138">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-140">若 **為 TRUE**，則會啟用此實例，並可用來完成用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="cea4d-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-141">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="cea4d-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-144">這個屬性是由 [**MSFT \_ 提供者**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** 和 **HostingSpecification** 屬性中的值所組成。</span><span class="sxs-lookup"><span data-stu-id="cea4d-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="cea4d-145">這個屬性的值會指定 WMI 如何載入提供者，以及其執行所在的安全性帳戶。</span><span class="sxs-lookup"><span data-stu-id="cea4d-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="cea4d-146">如需設定 **HostingModel** 屬性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md) ，以及 [註冊提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="cea4d-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-148">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea4d-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-150">保留的。</span><span class="sxs-lookup"><span data-stu-id="cea4d-150">Reserved.</span></span> <span data-ttu-id="cea4d-151">預設值為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-152">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="cea4d-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea4d-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-155">提供序列化相關資訊的一組旗標。</span><span class="sxs-lookup"><span data-stu-id="cea4d-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="cea4d-156">預設值為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="cea4d-157">0</span><span class="sxs-lookup"><span data-stu-id="cea4d-157">0</span></span>
</dt> <dd>

<span data-ttu-id="cea4d-158">此提供者的所有初始化都必須序列化。</span><span class="sxs-lookup"><span data-stu-id="cea4d-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-159">1</span><span class="sxs-lookup"><span data-stu-id="cea4d-159">1</span></span>
</dt> <dd>

<span data-ttu-id="cea4d-160">在相同的命名空間中，此提供者的所有初始化都必須序列化。</span><span class="sxs-lookup"><span data-stu-id="cea4d-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-161">2</span><span class="sxs-lookup"><span data-stu-id="cea4d-161">2</span></span>
</dt> <dd>

<span data-ttu-id="cea4d-162">不需要初始化序列化。</span><span class="sxs-lookup"><span data-stu-id="cea4d-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cea4d-163">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="cea4d-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-164">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea4d-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-166">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-167">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="cea4d-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-170">TBD</span><span class="sxs-lookup"><span data-stu-id="cea4d-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-171">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cea4d-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-174">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="cea4d-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-175">提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="cea4d-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-176">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="cea4d-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-177">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea4d-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-179">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-180">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="cea4d-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-181">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-183">若 **為 TRUE**，當使用者使用不同的地區設定連接到相同的命名空間時，就會為每個地區設定初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="cea4d-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="cea4d-184">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-185">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="cea4d-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-186">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-188">若 **為 TRUE**，則會為每個 NT LAN Manager 初始化一次提供者 (NTLM) 使用者來對提供者提出要求。</span><span class="sxs-lookup"><span data-stu-id="cea4d-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="cea4d-189">如果 **為 FALSE** (預設) ，則提供者會針對所有使用者初始化一次。</span><span class="sxs-lookup"><span data-stu-id="cea4d-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-190">**純**</span><span class="sxs-lookup"><span data-stu-id="cea4d-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-191">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-193">若 **為 TRUE**，當 WMI 呼叫其主要介面的 **發行** 方法時，提供者同意在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，以準備卸載。</span><span class="sxs-lookup"><span data-stu-id="cea4d-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="cea4d-194">必須保持 WMI 用戶端無法作為提供者的提供者，應該將 **純** 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="cea4d-195">預設設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="cea4d-196">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="cea4d-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cea4d-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea4d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-200">安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可決定可成功呼叫 IWbemDecoupledRegistrar 的一組使用者 [**：向**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) 低耦合提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="cea4d-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="cea4d-201">如需詳細資訊，請參閱 Windows SDK 的安全性一節中的「 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 」主題。</span><span class="sxs-lookup"><span data-stu-id="cea4d-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="cea4d-202">此安全描述項僅供低耦合提供者使用，且不會影響其他提供者。</span><span class="sxs-lookup"><span data-stu-id="cea4d-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="cea4d-203">如需詳細資訊，請參閱 [將提供者併入應用程式](incorporating-a-provider-in-an-application.md)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="cea4d-204">WMI 會針對使用 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemObjectSink**](iwbemobjectsink.md) 介面的低耦合提供者執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="cea4d-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="cea4d-205">如果安全描述項為 **Null**，則只有在 LocalSystem、NetworkService、LocalService 帳戶下執行的應用程式或服務可以執行低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="cea4d-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="cea4d-206">下列字串顯示只有內建系統管理員才能執行的低耦合提供者。」O:BAG：不正確： (A;; 0x1;;;BA) 」</span><span class="sxs-lookup"><span data-stu-id="cea4d-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="cea4d-207">如需設定 **SecurityDescriptor** 屬性的詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-208">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="cea4d-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-209">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-210">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-211">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-212">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="cea4d-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-213">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-215">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-216">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="cea4d-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-217">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-218">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-219">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-220">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="cea4d-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-221">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-222">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-223">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-224">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="cea4d-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-225">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-227">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-228">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="cea4d-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-229">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea4d-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-230">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-231">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea4d-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-232">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="cea4d-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-233">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea4d-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-234">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-235">[日期和時間格式](date-and-time-format.md) ，指定 WMI 允許提供者在卸載之前保持閒置的時間長度。</span><span class="sxs-lookup"><span data-stu-id="cea4d-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="cea4d-236">一般而言，提供者會要求 WMI 等待時間不超過五分鐘。</span><span class="sxs-lookup"><span data-stu-id="cea4d-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="cea4d-237">針對目前版本的 WMI，會忽略這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cea4d-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="cea4d-238">WMI 會根據根命名空間內部類別中的超時值來卸載提供者 \\ 。</span><span class="sxs-lookup"><span data-stu-id="cea4d-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="cea4d-239">建議提供者設定 **UnloadTimeout**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="cea4d-240">如需詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="cea4d-241">**版本**</span><span class="sxs-lookup"><span data-stu-id="cea4d-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea4d-242">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cea4d-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea4d-243">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea4d-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea4d-244">提供者的版本。</span><span class="sxs-lookup"><span data-stu-id="cea4d-244">Version of the provider.</span></span> <span data-ttu-id="cea4d-245">支援的版本為1和2。</span><span class="sxs-lookup"><span data-stu-id="cea4d-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="cea4d-246">第2版可針對所有相關聯的屬性註冊增強有效性檢查，特別是 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="cea4d-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cea4d-247">備註</span><span class="sxs-lookup"><span data-stu-id="cea4d-247">Remarks</span></span>

<span data-ttu-id="cea4d-248">**\_ \_ Win32Provider** 類別衍生自 [**\_ \_ Provider**](--provider.md)。</span><span class="sxs-lookup"><span data-stu-id="cea4d-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="cea4d-249">大部分的提供者可以接受 **InitializationReentrancy** 屬性的預設值。</span><span class="sxs-lookup"><span data-stu-id="cea4d-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="cea4d-250">但是，如果提供者可以針對個別使用者支援同時初始化，則這個屬性可以設定為 1 (一個) 。</span><span class="sxs-lookup"><span data-stu-id="cea4d-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="cea4d-251">如果需要序列化初始化， **InitializationReentrancy** 會維持 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="cea4d-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="cea4d-252">在這兩個實例中， **PerUserInitialization** 會設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cea4d-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="cea4d-253">純粹提供者或提供者將 **純** 虛擬屬性設定為 **TRUE**，只存在於來自應用程式和 WMI 的服務要求。</span><span class="sxs-lookup"><span data-stu-id="cea4d-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="cea4d-254">大部分的提供者都是純服務提供者。</span><span class="sxs-lookup"><span data-stu-id="cea4d-254">Most providers are pure providers.</span></span> <span data-ttu-id="cea4d-255">Nonpure 提供者是例外狀況。</span><span class="sxs-lookup"><span data-stu-id="cea4d-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="cea4d-256">Nonpure 提供者在完成服務要求之後，會轉換成用戶端的角色。</span><span class="sxs-lookup"><span data-stu-id="cea4d-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="cea4d-257">Nonpure 提供者的範例是開始發出查詢的推播提供者，並在完成初始化之後發出 WMI 要求。</span><span class="sxs-lookup"><span data-stu-id="cea4d-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="cea4d-258">除了在初始化時以資料更新 CIM 存放庫，推送提供者沒有任何責任。</span><span class="sxs-lookup"><span data-stu-id="cea4d-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="cea4d-259">更新存放庫之後，推播提供者可以等候卸載，或轉換為用戶端的角色。</span><span class="sxs-lookup"><span data-stu-id="cea4d-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="cea4d-260">等候卸載的推播提供者是純粹的提供者。</span><span class="sxs-lookup"><span data-stu-id="cea4d-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="cea4d-261">參與用戶端活動的推送提供者為 nonpure。</span><span class="sxs-lookup"><span data-stu-id="cea4d-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="cea4d-262">WMI 必須能夠區分純的提供者與非單純的提供者，讓它能夠判斷何時可以安全地關閉。</span><span class="sxs-lookup"><span data-stu-id="cea4d-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="cea4d-263">WMI 必須等待所有涉及非純提供者的作業完成，才能安全地關閉。</span><span class="sxs-lookup"><span data-stu-id="cea4d-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea4d-264">規格需求</span><span class="sxs-lookup"><span data-stu-id="cea4d-264">Requirements</span></span>



| <span data-ttu-id="cea4d-265">需求</span><span class="sxs-lookup"><span data-stu-id="cea4d-265">Requirement</span></span> | <span data-ttu-id="cea4d-266">值</span><span class="sxs-lookup"><span data-stu-id="cea4d-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="cea4d-267">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cea4d-267">Minimum supported client</span></span><br/> | <span data-ttu-id="cea4d-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cea4d-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="cea4d-269">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cea4d-269">Minimum supported server</span></span><br/> | <span data-ttu-id="cea4d-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cea4d-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="cea4d-271">命名空間</span><span class="sxs-lookup"><span data-stu-id="cea4d-271">Namespace</span></span><br/>                | <span data-ttu-id="cea4d-272">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="cea4d-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="cea4d-273">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cea4d-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea4d-274">**\_\_提供者**</span><span class="sxs-lookup"><span data-stu-id="cea4d-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="cea4d-275">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="cea4d-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="cea4d-276">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="cea4d-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

