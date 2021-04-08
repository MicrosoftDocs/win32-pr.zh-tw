---
description: 在 WMI 中註冊類別提供者。
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: __ClassProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695615"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="08959-103">\_\_ClassProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="08959-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="08959-104">**\_ \_ ClassProviderRegistration** 系統類別會在 WMI 中註冊類別提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="08959-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="08959-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08959-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="08959-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08959-107">語法</span><span class="sxs-lookup"><span data-stu-id="08959-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="08959-108">成員</span><span class="sxs-lookup"><span data-stu-id="08959-108">Members</span></span>

<span data-ttu-id="08959-109">**\_ \_ ClassProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="08959-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="08959-110">屬性</span><span class="sxs-lookup"><span data-stu-id="08959-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08959-111">屬性</span><span class="sxs-lookup"><span data-stu-id="08959-111">Properties</span></span>

<span data-ttu-id="08959-112">**\_ \_ ClassProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="08959-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08959-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="08959-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-114">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="08959-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08959-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="08959-117">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="08959-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="08959-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08959-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-120">指出類別或執行個體提供者是否提供資料，或是依賴 WMI 和通用訊息模型 (CIM) 存放庫。</span><span class="sxs-lookup"><span data-stu-id="08959-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="08959-121">提取提供者支援對資料進行動態存取，而推送提供者則會將資料儲存在 CIM 存放庫中，並依賴 WMI 來提供其存取權。</span><span class="sxs-lookup"><span data-stu-id="08959-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="08959-122">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="08959-122">The default value is 0 (zero).</span></span> <span data-ttu-id="08959-123">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="08959-124">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="08959-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**提取** (0) </span><span class="sxs-lookup"><span data-stu-id="08959-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08959-126">提供者是提取提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="08959-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**推送** (1) </span><span class="sxs-lookup"><span data-stu-id="08959-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08959-128">提供者是推播提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="08959-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2) </span><span class="sxs-lookup"><span data-stu-id="08959-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08959-130">提供者是推播驗證的提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="08959-131">請注意，目前不支援 **PushVerify** 提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-132">**PerUserSchema**</span><span class="sxs-lookup"><span data-stu-id="08959-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-133">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-135">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="08959-136">**供應商**</span><span class="sxs-lookup"><span data-stu-id="08959-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-137">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="08959-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="08959-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="08959-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08959-139">類別提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="08959-139">Object path to a class provider.</span></span> <span data-ttu-id="08959-140">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="08959-141">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="08959-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-142">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="08959-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08959-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-144">提供者類型的陣列，包含查詢處理的支援。</span><span class="sxs-lookup"><span data-stu-id="08959-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="08959-145">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="08959-146">需要類別提供者才能支援至少一種查詢。</span><span class="sxs-lookup"><span data-stu-id="08959-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="08959-147">如果執行個體提供者不支援查詢處理，則可以將 **QuerySupportLevels** 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="08959-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="08959-148">支援查詢的提供者會執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法，並將此屬性設定為下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="08959-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="08959-149"> ( "WQL： UnarySelect" ) </span><span class="sxs-lookup"><span data-stu-id="08959-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08959-150"> ( "WQL： References" ) </span><span class="sxs-lookup"><span data-stu-id="08959-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08959-151"> ( "WQL： Associators of" ) </span><span class="sxs-lookup"><span data-stu-id="08959-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08959-152"> ( "WQL： V1ProviderDefined" ) </span><span class="sxs-lookup"><span data-stu-id="08959-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-153">**ReferencedSetQueries**</span><span class="sxs-lookup"><span data-stu-id="08959-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-154">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="08959-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08959-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-156">描述類別提供者所支援之參考類別集的一或多個查詢。</span><span class="sxs-lookup"><span data-stu-id="08959-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="08959-157">可以提供關聯類別的提供者必須在這個屬性中至少包含一個查詢。</span><span class="sxs-lookup"><span data-stu-id="08959-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="08959-158">**ResultSetQueries**</span><span class="sxs-lookup"><span data-stu-id="08959-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-159">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="08959-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08959-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-161">一或多個查詢，描述可由類別提供者提供的所有類別集，或這些類別的超集合。</span><span class="sxs-lookup"><span data-stu-id="08959-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="08959-162">這個屬性永遠不會指定支援類別的子集。</span><span class="sxs-lookup"><span data-stu-id="08959-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="08959-163">**ReSynchroniseOnNamespaceOpen**</span><span class="sxs-lookup"><span data-stu-id="08959-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-164">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-166">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="08959-167">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="08959-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-168">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-170">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-170">Not used.</span></span>

<span data-ttu-id="08959-171">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="08959-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="08959-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-173">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-175">若 **為 TRUE**，表示提供者支援資料刪除。</span><span class="sxs-lookup"><span data-stu-id="08959-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="08959-176">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="08959-177"> (True) </span><span class="sxs-lookup"><span data-stu-id="08959-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="08959-178">提供者可透過執行下列其中一個 [**iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (類別提供者) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (執行個體提供者) ，來支援類別或實例的刪除。</span><span class="sxs-lookup"><span data-stu-id="08959-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="08959-179"> (False) </span><span class="sxs-lookup"><span data-stu-id="08959-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="08959-180">提供者不支援資料刪除，並傳回無法從 [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)或 [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="08959-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-181">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="08959-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-182">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-184">若 **為 TRUE**，表示提供者支援資料列舉。</span><span class="sxs-lookup"><span data-stu-id="08959-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="08959-185">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="08959-186"> (True) </span><span class="sxs-lookup"><span data-stu-id="08959-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="08959-187">提供者支援資料列舉，方法是實作為) 的 [**iwbemservices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (類別提供者的其中一個，或) 的 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="08959-188"> (False) </span><span class="sxs-lookup"><span data-stu-id="08959-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="08959-189">提供者不支援資料列舉，並且會傳回無法從 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)或 [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="08959-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-190">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="08959-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-191">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-193">若 **為 TRUE**，則類別或執行個體提供者支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="08959-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="08959-194">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="08959-195"> (True) </span><span class="sxs-lookup"><span data-stu-id="08959-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="08959-196">提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="08959-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="08959-197"> (False) </span><span class="sxs-lookup"><span data-stu-id="08959-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="08959-198">提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="08959-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-199">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="08959-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-200">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-202">若 **為 TRUE**，則類別或執行個體提供者支援資料修改。</span><span class="sxs-lookup"><span data-stu-id="08959-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="08959-203">這個屬性繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="08959-204"> (True) </span><span class="sxs-lookup"><span data-stu-id="08959-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="08959-205">提供者支援類別或實例修改，方法是執行 [**iwbemservices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) 中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="08959-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="08959-206"> (False) </span><span class="sxs-lookup"><span data-stu-id="08959-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="08959-207">提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="08959-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08959-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="08959-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-209">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-210">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-211">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="08959-212">**SuppportsBatching**</span><span class="sxs-lookup"><span data-stu-id="08959-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-213">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="08959-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08959-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-215">未使用。</span><span class="sxs-lookup"><span data-stu-id="08959-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="08959-216">**UnsupportedQueries**</span><span class="sxs-lookup"><span data-stu-id="08959-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-217">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="08959-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08959-218">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-219">描述類別提供者不支援的一組類別的一或多個查詢。</span><span class="sxs-lookup"><span data-stu-id="08959-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="08959-220">您可以使用這個屬性來減去 **ResultSetQueries** 所隱含的一組類別。</span><span class="sxs-lookup"><span data-stu-id="08959-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="08959-221">**版本**</span><span class="sxs-lookup"><span data-stu-id="08959-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08959-222">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="08959-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08959-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="08959-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08959-224">此類別提供者的版本。</span><span class="sxs-lookup"><span data-stu-id="08959-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08959-225">備註</span><span class="sxs-lookup"><span data-stu-id="08959-225">Remarks</span></span>

<span data-ttu-id="08959-226">**\_ \_ ClassProviderRegistration** 類別衍生自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)，它衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="08959-227">繼承自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)的屬性會指出類別提供者是否支援資料抓取、修改、刪除、列舉和查詢處理。</span><span class="sxs-lookup"><span data-stu-id="08959-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="08959-228">**InteractionType** 屬性會指定類別提供者是否設計為提取或推入提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="08959-229">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="08959-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="08959-230">[**\_ \_ ProviderRegistration**](--providerregistration.md)類別會定義 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)屬性。</span><span class="sxs-lookup"><span data-stu-id="08959-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="08959-231">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ ClassProviderRegistration** 的實例來註冊提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="08959-232">只有系統管理員可以刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="08959-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="08959-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="08959-233">Requirements</span></span>



| <span data-ttu-id="08959-234">需求</span><span class="sxs-lookup"><span data-stu-id="08959-234">Requirement</span></span> | <span data-ttu-id="08959-235">值</span><span class="sxs-lookup"><span data-stu-id="08959-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="08959-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08959-236">Minimum supported client</span></span><br/> | <span data-ttu-id="08959-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08959-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="08959-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08959-238">Minimum supported server</span></span><br/> | <span data-ttu-id="08959-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08959-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="08959-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="08959-240">Namespace</span></span><br/>                | <span data-ttu-id="08959-241">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="08959-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="08959-242">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08959-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08959-243">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="08959-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="08959-244">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="08959-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="08959-245">註冊類別提供者</span><span class="sxs-lookup"><span data-stu-id="08959-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="08959-246">註冊執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="08959-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="08959-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="08959-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

