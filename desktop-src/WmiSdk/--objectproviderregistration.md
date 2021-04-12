---
description: 作為類別的父類別，用來在 WMI 中註冊類別和執行個體提供者。
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: __ObjectProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319336"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="ffe79-103">\_\_ObjectProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="ffe79-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="ffe79-104">**\_ \_ ObjectProviderRegistration** 抽象系統類別可作為類別的父類別，用來在 WMI 中註冊類別和執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="ffe79-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe79-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ffe79-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="ffe79-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe79-107">語法</span><span class="sxs-lookup"><span data-stu-id="ffe79-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="ffe79-108">成員</span><span class="sxs-lookup"><span data-stu-id="ffe79-108">Members</span></span>

<span data-ttu-id="ffe79-109">**\_ \_ ObjectProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ffe79-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="ffe79-110">屬性</span><span class="sxs-lookup"><span data-stu-id="ffe79-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffe79-111">屬性</span><span class="sxs-lookup"><span data-stu-id="ffe79-111">Properties</span></span>

<span data-ttu-id="ffe79-112">**\_ \_ ObjectProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe79-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffe79-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="ffe79-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-114">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ffe79-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-116">指出類別或執行個體提供者是否提供本身的資料，或依賴 WMI 和通用訊息模型 (CIM) 存放庫。</span><span class="sxs-lookup"><span data-stu-id="ffe79-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="ffe79-117">提取提供者支援對其資料進行動態存取，而推送提供者會將其資料儲存在 CIM 存放庫中，並依賴 WMI 來提供其存取權。</span><span class="sxs-lookup"><span data-stu-id="ffe79-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="ffe79-118">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe79-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="ffe79-119">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="ffe79-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="ffe79-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**提取** (0) </span><span class="sxs-lookup"><span data-stu-id="ffe79-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ffe79-121">提供者是提取提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="ffe79-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**推送** (1) </span><span class="sxs-lookup"><span data-stu-id="ffe79-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ffe79-123">提供者是推播提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="ffe79-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2) </span><span class="sxs-lookup"><span data-stu-id="ffe79-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ffe79-125">提供者是推播驗證的提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="ffe79-126">請注意，目前不支援推播驗證。</span><span class="sxs-lookup"><span data-stu-id="ffe79-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ffe79-127">**供應商**</span><span class="sxs-lookup"><span data-stu-id="ffe79-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-128">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="ffe79-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ffe79-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-130">[**\_ \_ 提供者**](--provider.md)實例的參考，代表物件提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="ffe79-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="ffe79-131">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe79-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="ffe79-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="ffe79-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-135">提供者類型的陣列，包含查詢處理的支援。</span><span class="sxs-lookup"><span data-stu-id="ffe79-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="ffe79-136">類別提供者不支援任何類型的查詢。</span><span class="sxs-lookup"><span data-stu-id="ffe79-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="ffe79-137">如果執行個體提供者不支援查詢處理，則可以將 **QuerySupportLevels** 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="ffe79-138">支援查詢的提供者會執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法，並將此屬性設定為下列其中一個或多個值 (屬性類型是陣列) 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="ffe79-139">"WQL： UnarySelect"</span><span class="sxs-lookup"><span data-stu-id="ffe79-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="ffe79-140">"WQL： References"</span><span class="sxs-lookup"><span data-stu-id="ffe79-140">"WQL:References"</span></span>

<span data-ttu-id="ffe79-141">"WQL： Associators of"</span><span class="sxs-lookup"><span data-stu-id="ffe79-141">"WQL:Associators"</span></span>

<span data-ttu-id="ffe79-142">"WQL： V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="ffe79-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="ffe79-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="ffe79-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="ffe79-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-150">若 **為 True**，表示提供者支援資料刪除。</span><span class="sxs-lookup"><span data-stu-id="ffe79-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="ffe79-151">對</span><span class="sxs-lookup"><span data-stu-id="ffe79-151">True</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-152">提供者可透過執行下列其中一個 [**iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (類別提供者) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (執行個體提供者) ，來支援類別或實例的刪除。</span><span class="sxs-lookup"><span data-stu-id="ffe79-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-153">否</span><span class="sxs-lookup"><span data-stu-id="ffe79-153">False</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-154">提供者不支援資料刪除，並傳回無法從 [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)或 [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ffe79-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="ffe79-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-156">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-158">若 **為 True**，表示提供者支援資料列舉。</span><span class="sxs-lookup"><span data-stu-id="ffe79-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="ffe79-159">對</span><span class="sxs-lookup"><span data-stu-id="ffe79-159">True</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-160">提供者支援資料列舉，方法是實作為) 的 [**iwbemservices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (類別提供者的其中一個，或) 的 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-161">否</span><span class="sxs-lookup"><span data-stu-id="ffe79-161">False</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-162">提供者不支援資料列舉，並且會傳回無法從 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)或 [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ffe79-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="ffe79-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-164">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-166">若 **為 True**，則類別或執行個體提供者支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="ffe79-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="ffe79-167">對</span><span class="sxs-lookup"><span data-stu-id="ffe79-167">True</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-168">提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="ffe79-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-169">否</span><span class="sxs-lookup"><span data-stu-id="ffe79-169">False</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-170">提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ffe79-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="ffe79-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-174">若 **為 True**，則類別或執行個體提供者支援資料修改。</span><span class="sxs-lookup"><span data-stu-id="ffe79-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="ffe79-175">對</span><span class="sxs-lookup"><span data-stu-id="ffe79-175">True</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-176">提供者支援類別或實例修改，方法是執行 [**iwbemservices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) 中的其中一個。</span><span class="sxs-lookup"><span data-stu-id="ffe79-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="ffe79-177">否</span><span class="sxs-lookup"><span data-stu-id="ffe79-177">False</span></span>
</dt> <dd>

<span data-ttu-id="ffe79-178">提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="ffe79-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ffe79-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="ffe79-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffe79-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ffe79-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ffe79-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ffe79-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ffe79-182">未使用。</span><span class="sxs-lookup"><span data-stu-id="ffe79-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffe79-183">備註</span><span class="sxs-lookup"><span data-stu-id="ffe79-183">Remarks</span></span>

<span data-ttu-id="ffe79-184">**\_ \_ ObjectProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe79-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="ffe79-185">類別提供者必須將 **SupportsEnumeration** 屬性設定為 **True** ，因為提供者必須能夠提供 WMI 及其類別清單。</span><span class="sxs-lookup"><span data-stu-id="ffe79-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="ffe79-186">如果類別提供者嘗試將此屬性設定為 **False**，WMI 會將註冊標示為不合法。</span><span class="sxs-lookup"><span data-stu-id="ffe79-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="ffe79-187">執行個體提供者不需要支援列舉，而且可以選擇將 **SupportsEnumeration** 設為 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="ffe79-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="ffe79-188">將 **QuerySupportLevels** 設定為 "WQL： UnarySelect" 的提供者可以接受由 WMI 1.0 版所支援的基本 SELECT 語句所組成的查詢。</span><span class="sxs-lookup"><span data-stu-id="ffe79-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="ffe79-189">類別和執行個體提供者都應該能夠處理 **\_ \_ 類別** 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="ffe79-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="ffe79-190">類別提供者也預期會處理 **\_ \_ 超級類別** 系統屬性和 ISA 運算子。</span><span class="sxs-lookup"><span data-stu-id="ffe79-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="ffe79-191">ISA 運算子用來將結果集展開至衍生的類別。</span><span class="sxs-lookup"><span data-stu-id="ffe79-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="ffe79-192">如果提供者無法解讀的查詢，它會要求 WMI 處理它，方法是傳回 **WBEM \_ 電子 \_ 太 \_ 複雜** 的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="ffe79-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="ffe79-193">如需有效 WQL 語法的說明，請參閱 [使用 Wql 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe79-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="ffe79-194">將 **QuerySupportLevels** 設定為 **WQL： V1ProviderDefined** 的提供者可以嘗試支援一組較大的 SQL 語法，其本身的風險包括 `ORDER BY` 子句。</span><span class="sxs-lookup"><span data-stu-id="ffe79-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="ffe79-195">WMI 不會解讀其他子句，或嘗試確定結果集是否正確。</span><span class="sxs-lookup"><span data-stu-id="ffe79-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="ffe79-196">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例並註冊，來註冊或刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe79-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe79-197">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe79-197">Requirements</span></span>



| <span data-ttu-id="ffe79-198">需求</span><span class="sxs-lookup"><span data-stu-id="ffe79-198">Requirement</span></span> | <span data-ttu-id="ffe79-199">值</span><span class="sxs-lookup"><span data-stu-id="ffe79-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ffe79-200">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffe79-200">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe79-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffe79-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ffe79-202">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffe79-202">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe79-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffe79-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ffe79-204">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffe79-204">Namespace</span></span><br/>                | <span data-ttu-id="ffe79-205">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="ffe79-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ffe79-206">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe79-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe79-207">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="ffe79-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="ffe79-208">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="ffe79-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ffe79-209">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="ffe79-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

