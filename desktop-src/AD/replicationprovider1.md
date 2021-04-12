---
title: ReplicationProvider1 類別
description: 提供者實例的基類。
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- ReplicationProvider1 類別 Active Directory
- ReplicationProvider1 類別 Active Directory，說明
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025002"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="cea04-105">ReplicationProvider1 類別</span><span class="sxs-lookup"><span data-stu-id="cea04-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="cea04-106">提供者實例的基類。</span><span class="sxs-lookup"><span data-stu-id="cea04-106">The base class for the provider instance.</span></span>

<span data-ttu-id="cea04-107">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="cea04-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea04-108">語法</span><span class="sxs-lookup"><span data-stu-id="cea04-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="cea04-109">成員</span><span class="sxs-lookup"><span data-stu-id="cea04-109">Members</span></span>

<span data-ttu-id="cea04-110">**ReplicationProvider1** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="cea04-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="cea04-111">屬性</span><span class="sxs-lookup"><span data-stu-id="cea04-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cea04-112">屬性</span><span class="sxs-lookup"><span data-stu-id="cea04-112">Properties</span></span>

<span data-ttu-id="cea04-113">**ReplicationProvider1** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="cea04-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cea04-114">**ClientLoadableCLSID**</span><span class="sxs-lookup"><span data-stu-id="cea04-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-117">WMI 用來判斷是否要將高效能提供者載入至用戶端進程或 WMI 進程的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="cea04-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="cea04-118">如果提供者和用戶端都位於相同的電腦上，WMI 會使用 **ClientLoadableCLSID** 做為類別識別碼，將處理常式載入至用戶端。</span><span class="sxs-lookup"><span data-stu-id="cea04-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="cea04-119">當提供者和用戶端位於不同的電腦上時，WMI 會將提供者載入至 WMI。</span><span class="sxs-lookup"><span data-stu-id="cea04-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="cea04-120">WMI 也會使用 **ClientLoadableCLSID** 來支援重新整理作業。</span><span class="sxs-lookup"><span data-stu-id="cea04-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="cea04-121">如需詳細資訊，請參閱 [註冊 High-Performance 提供者。](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="cea04-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="cea04-122">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-123">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="cea04-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-126">**GUID** ，表示提供者 COM 物件 (**CLSID**) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="cea04-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="cea04-127">這個 COM 物件必須包含 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 介面的實作為。</span><span class="sxs-lookup"><span data-stu-id="cea04-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="cea04-128">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-129">**並行**</span><span class="sxs-lookup"><span data-stu-id="cea04-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-130">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea04-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-132">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-132">Not used.</span></span>

<span data-ttu-id="cea04-133">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-134">**DefaultMachineName**</span><span class="sxs-lookup"><span data-stu-id="cea04-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-137">識別要啟動提供者的電腦。</span><span class="sxs-lookup"><span data-stu-id="cea04-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="cea04-138">如果提供者在本機電腦上執行，則為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cea04-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="cea04-139">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="cea04-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-141">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-143">若 **為 TRUE**，則會啟用此實例，並可用來完成用戶端要求。</span><span class="sxs-lookup"><span data-stu-id="cea04-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="cea04-144">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-145">**HostingModel**</span><span class="sxs-lookup"><span data-stu-id="cea04-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="cea04-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cea04-148">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "HostingModel" ) </span><span class="sxs-lookup"><span data-stu-id="cea04-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="cea04-149">包含提供者的裝載模型。</span><span class="sxs-lookup"><span data-stu-id="cea04-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="cea04-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="cea04-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-151">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea04-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-153">保留的。</span><span class="sxs-lookup"><span data-stu-id="cea04-153">Reserved.</span></span> <span data-ttu-id="cea04-154">預設值為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="cea04-154">The default value is zero (0).</span></span>

<span data-ttu-id="cea04-155">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-156">**InitializationReentrancy**</span><span class="sxs-lookup"><span data-stu-id="cea04-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-157">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="cea04-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-159">提供序列化相關資訊的一組旗標。</span><span class="sxs-lookup"><span data-stu-id="cea04-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="cea04-160">預設值為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="cea04-160">The default value is zero (0).</span></span>

<span data-ttu-id="cea04-161">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cea04-162"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="cea04-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cea04-163">此提供者的所有初始化都必須序列化。</span><span class="sxs-lookup"><span data-stu-id="cea04-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="cea04-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="cea04-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="cea04-165">在相同的命名空間中，此提供者的所有初始化都必須序列化。</span><span class="sxs-lookup"><span data-stu-id="cea04-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="cea04-166"><span id="2"></span>**二級**</span><span class="sxs-lookup"><span data-stu-id="cea04-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="cea04-167">不需要初始化序列化。</span><span class="sxs-lookup"><span data-stu-id="cea04-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cea04-168">**InitializationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="cea04-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-169">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea04-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-171">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-171">Not used.</span></span>

<span data-ttu-id="cea04-172">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-173">**InitializeAsAdminFirst**</span><span class="sxs-lookup"><span data-stu-id="cea04-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-174">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-176">**Windows Server 2003：** 這個屬性已停用。</span><span class="sxs-lookup"><span data-stu-id="cea04-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="cea04-177">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-178">**名稱**</span><span class="sxs-lookup"><span data-stu-id="cea04-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cea04-181">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cea04-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cea04-182">提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="cea04-182">The provider name.</span></span>

<span data-ttu-id="cea04-183">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-184">**OperationTimeoutInterval**</span><span class="sxs-lookup"><span data-stu-id="cea04-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-185">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea04-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-186">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-187">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-187">Not used.</span></span>

<span data-ttu-id="cea04-188">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-189">**PerLocaleInitialization**</span><span class="sxs-lookup"><span data-stu-id="cea04-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-190">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-192">若 **為 TRUE**，當使用者使用不同的地區設定連接到相同的命名空間時，就會為每個地區設定初始化提供者。</span><span class="sxs-lookup"><span data-stu-id="cea04-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="cea04-193">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cea04-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="cea04-194">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-195">**PerUserInitialization**</span><span class="sxs-lookup"><span data-stu-id="cea04-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-196">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-198">若 **為 TRUE**，則會為每個 NT LAN Manager 初始化一次提供者 (NTLM) 使用者來對提供者提出要求。</span><span class="sxs-lookup"><span data-stu-id="cea04-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="cea04-199">如果 **為 FALSE** (預設) ，則提供者會針對所有使用者初始化一次。</span><span class="sxs-lookup"><span data-stu-id="cea04-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="cea04-200">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-201">**純**</span><span class="sxs-lookup"><span data-stu-id="cea04-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-202">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-203">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-204">若 **為 TRUE**，當 WMI 呼叫其主要介面的 **發行** 方法時，提供者同意在所有未完成的介面點上呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，以準備卸載。</span><span class="sxs-lookup"><span data-stu-id="cea04-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="cea04-205">必須保持 WMI 用戶端無法作為提供者的提供者，應該將 **純** 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cea04-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="cea04-206">預設設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cea04-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="cea04-207">如需詳細資訊，請參閱本主題的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="cea04-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="cea04-208">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="cea04-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cea04-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-212">安全描述項定義語言中的安全描述項 (SD)  (SDDL) ，可決定可成功呼叫 IWbemDecoupledRegistrar 的一組使用者 [**：向**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) 低耦合提供者註冊。</span><span class="sxs-lookup"><span data-stu-id="cea04-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="cea04-213">如需詳細資訊，請參閱 Windows SDK 的安全性一節中的「 [安全描述項定義語言](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 」主題。</span><span class="sxs-lookup"><span data-stu-id="cea04-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="cea04-214">此安全描述項僅供低耦合提供者使用，且不會影響其他提供者。</span><span class="sxs-lookup"><span data-stu-id="cea04-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="cea04-215">如需詳細資訊，請參閱 [將提供者併入應用程式](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application)。</span><span class="sxs-lookup"><span data-stu-id="cea04-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="cea04-216">WMI 會針對使用 [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) 和 [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) 介面的低耦合提供者執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="cea04-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="cea04-217">如果安全描述項為 **Null**，則只有在 LocalSystem、NetworkService、LocalService 帳戶下執行的應用程式或服務可以執行低耦合提供者。</span><span class="sxs-lookup"><span data-stu-id="cea04-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="cea04-218">下列字串顯示只有內建系統管理員才能執行的低耦合提供者。」O:BAG：不正確： (A;; 0x1;;;BA) 」</span><span class="sxs-lookup"><span data-stu-id="cea04-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="cea04-219">如需設定 **SecurityDescriptor** 屬性的詳細資訊，請參閱 [維護 WMI 安全性](/windows/desktop/WmiSdk/maintaining-wmi-security)。</span><span class="sxs-lookup"><span data-stu-id="cea04-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="cea04-220">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-221">**SupportsExplicitShutdown**</span><span class="sxs-lookup"><span data-stu-id="cea04-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-222">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-224">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-224">Not used.</span></span>

<span data-ttu-id="cea04-225">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-226">**SupportsExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="cea04-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-227">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-228">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-229">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-229">Not used.</span></span>

<span data-ttu-id="cea04-230">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-231">**SupportsQuotas**</span><span class="sxs-lookup"><span data-stu-id="cea04-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-232">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-233">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-234">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-234">Not used.</span></span>

<span data-ttu-id="cea04-235">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-236">**SupportsSendStatus**</span><span class="sxs-lookup"><span data-stu-id="cea04-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-237">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-239">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-239">Not used.</span></span>

<span data-ttu-id="cea04-240">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-241">**SupportsShutdown**</span><span class="sxs-lookup"><span data-stu-id="cea04-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-242">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-243">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-244">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-244">Not used.</span></span>

<span data-ttu-id="cea04-245">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-246">**SupportsThrottling**</span><span class="sxs-lookup"><span data-stu-id="cea04-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-247">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="cea04-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-248">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-249">未使用。</span><span class="sxs-lookup"><span data-stu-id="cea04-249">Not used.</span></span>

<span data-ttu-id="cea04-250">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-251">**UnloadTimeout**</span><span class="sxs-lookup"><span data-stu-id="cea04-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-252">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="cea04-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-254">[日期和時間格式](/windows/desktop/WmiSdk/date-and-time-format) ，指定 WMI 允許提供者在卸載之前保持閒置的時間長度。</span><span class="sxs-lookup"><span data-stu-id="cea04-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="cea04-255">一般而言，提供者會要求 WMI 等待時間不超過五分鐘。</span><span class="sxs-lookup"><span data-stu-id="cea04-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="cea04-256">針對目前版本的 WMI，會忽略這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cea04-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="cea04-257">WMI 會根據根命名空間內部類別中的超時值來卸載提供者 \\ 。</span><span class="sxs-lookup"><span data-stu-id="cea04-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="cea04-258">建議提供者設定 **UnloadTimeout**。</span><span class="sxs-lookup"><span data-stu-id="cea04-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="cea04-259">如需詳細資訊，請參閱卸載 [提供者](/windows/desktop/WmiSdk/unloading-a-provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="cea04-260">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="cea04-261">**版本**</span><span class="sxs-lookup"><span data-stu-id="cea04-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cea04-262">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cea04-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cea04-263">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cea04-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="cea04-264">提供者的版本。</span><span class="sxs-lookup"><span data-stu-id="cea04-264">Version of the provider.</span></span> <span data-ttu-id="cea04-265">支援的版本為1和2。</span><span class="sxs-lookup"><span data-stu-id="cea04-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="cea04-266">第2版可針對所有相關聯的屬性註冊增強有效性檢查，特別是 [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) 屬性。</span><span class="sxs-lookup"><span data-stu-id="cea04-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="cea04-267">這個屬性繼承自 [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider)。</span><span class="sxs-lookup"><span data-stu-id="cea04-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cea04-268">備註</span><span class="sxs-lookup"><span data-stu-id="cea04-268">Remarks</span></span>

<span data-ttu-id="cea04-269">此類別的實例代表 Active Directory 網域服務的 WMI 提供者。</span><span class="sxs-lookup"><span data-stu-id="cea04-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="cea04-270">預設值如下：</span><span class="sxs-lookup"><span data-stu-id="cea04-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="cea04-271">Name = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="cea04-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="cea04-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="cea04-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="cea04-273">HostingModel = "NetworkServiceHost"</span><span class="sxs-lookup"><span data-stu-id="cea04-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="cea04-274">規格需求</span><span class="sxs-lookup"><span data-stu-id="cea04-274">Requirements</span></span>



| <span data-ttu-id="cea04-275">需求</span><span class="sxs-lookup"><span data-stu-id="cea04-275">Requirement</span></span> | <span data-ttu-id="cea04-276">值</span><span class="sxs-lookup"><span data-stu-id="cea04-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea04-277">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cea04-277">Minimum supported client</span></span><br/> | <span data-ttu-id="cea04-278">都不支援</span><span class="sxs-lookup"><span data-stu-id="cea04-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cea04-279">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cea04-279">Minimum supported server</span></span><br/> | <span data-ttu-id="cea04-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cea04-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cea04-281">命名空間</span><span class="sxs-lookup"><span data-stu-id="cea04-281">Namespace</span></span><br/>                | <span data-ttu-id="cea04-282">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="cea04-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="cea04-283">MOF</span><span class="sxs-lookup"><span data-stu-id="cea04-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cea04-284"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="cea04-285">DLL</span><span class="sxs-lookup"><span data-stu-id="cea04-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea04-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea04-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea04-287">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cea04-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea04-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="cea04-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

