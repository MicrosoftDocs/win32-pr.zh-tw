---
description: 在 WMI 中註冊執行個體提供者。
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988316"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="2f1f5-103">\_\_InstanceProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="2f1f5-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="2f1f5-104">**\_ \_ InstanceProviderRegistration** 系統類別會在 WMI 中註冊執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="2f1f5-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2f1f5-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1f5-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f1f5-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="2f1f5-108">成員</span><span class="sxs-lookup"><span data-stu-id="2f1f5-108">Members</span></span>

<span data-ttu-id="2f1f5-109">**\_ \_ InstanceProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2f1f5-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="2f1f5-110">屬性</span><span class="sxs-lookup"><span data-stu-id="2f1f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f1f5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="2f1f5-111">Properties</span></span>

<span data-ttu-id="2f1f5-112">**\_ \_ InstanceProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f1f5-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-114">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-116">指出類別或執行個體提供者會提供資料，或從 WMI 和通用訊息模型 (CIM) 存放庫中取出資料。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="2f1f5-117">提取提供者支援動態存取其資料;和推送提供者會將其資料儲存在 CIM 存放庫中，並使用 WMI 來提供其存取權。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="2f1f5-118">如需詳細資訊，請參閱 [判斷推播或提取狀態](determining-push-or-pull-status.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="2f1f5-119">預設值是 0 (零)。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="2f1f5-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**提取** (0) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-121">提供者是提取提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="2f1f5-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**推送** (1) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-123">提供者是推播提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="2f1f5-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-125">提供者是推播驗證的提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="2f1f5-126">請注意，目前不支援推播驗證提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-127">**供應商**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-128">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="2f1f5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-130">[**\_ \_ 提供者**](--provider.md)實例的參考，表示執行個體提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="2f1f5-131">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f1f5-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-133">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="2f1f5-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-135">提供者類型的陣列，包含查詢處理的支援。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="2f1f5-136">類別提供者不支援所有類型的查詢。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="2f1f5-137">如果執行個體提供者不支援查詢處理，則可以將 **QuerySupportLevels** 設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="2f1f5-138">支援查詢的提供者會執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法，並將此屬性設定為下列其中一個或多個值。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="2f1f5-139"> ( "WQL： UnarySelect" ) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2f1f5-140"> ( "WQL： References" ) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2f1f5-141"> ( "WQL： Associators of" ) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2f1f5-142"> ( "WQL： V1ProviderDefined" ) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-144">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f1f5-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-148">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-150">若 **為 True**，表示提供者支援資料刪除。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="2f1f5-151">對</span><span class="sxs-lookup"><span data-stu-id="2f1f5-151">True</span></span>
</dt> <dd>

<span data-ttu-id="2f1f5-152">提供者藉由執行 [**iwbemservices：:D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (類別提供者) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (執行個體提供者) ，支援類別或實例的刪除。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="2f1f5-153">否</span><span class="sxs-lookup"><span data-stu-id="2f1f5-153">False</span></span>
</dt> <dd>

<span data-ttu-id="2f1f5-154">提供者不支援資料刪除，並傳回無法從 [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)或 [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-156">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-158">若 **為 True**，表示提供者支援資料列舉。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="2f1f5-159"> (True) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-160">提供者支援資料列舉，方法是實作為) 的 [**iwbemservices：： CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (類別提供者的其中一個，或) 的 [**Iwbemservices：： CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="2f1f5-161"> (False) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-162">提供者不支援資料列舉，並且會傳回無法從 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)或 [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-164">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-166">若 **為 True**，則類別或執行個體提供者支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="2f1f5-167">對</span><span class="sxs-lookup"><span data-stu-id="2f1f5-167">True</span></span>
</dt> <dd>

<span data-ttu-id="2f1f5-168">提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="2f1f5-169">否</span><span class="sxs-lookup"><span data-stu-id="2f1f5-169">False</span></span>
</dt> <dd>

<span data-ttu-id="2f1f5-170">提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-174">若 **為 True**，則類別或執行個體提供者支援資料修改。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="2f1f5-175"> (True) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-176">提供者藉由執行下列其中一種方法來支援類別或實例修改： [**iwbemservices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) 或 [**Iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="2f1f5-177"> (False) </span><span class="sxs-lookup"><span data-stu-id="2f1f5-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="2f1f5-178">提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2f1f5-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f1f5-180">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f1f5-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="2f1f5-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2f1f5-182">未使用。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f1f5-183">備註</span><span class="sxs-lookup"><span data-stu-id="2f1f5-183">Remarks</span></span>

<span data-ttu-id="2f1f5-184">**\_ \_ InstanceProviderRegistration** 類別衍生自 [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)，它衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="2f1f5-185">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ InstanceProviderRegistration** 的實例來註冊執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="2f1f5-186">只有系統管理員可以刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="2f1f5-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1f5-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f1f5-187">Requirements</span></span>



| <span data-ttu-id="2f1f5-188">需求</span><span class="sxs-lookup"><span data-stu-id="2f1f5-188">Requirement</span></span> | <span data-ttu-id="2f1f5-189">值</span><span class="sxs-lookup"><span data-stu-id="2f1f5-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2f1f5-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f1f5-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2f1f5-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f1f5-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2f1f5-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f1f5-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2f1f5-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f1f5-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2f1f5-194">命名空間</span><span class="sxs-lookup"><span data-stu-id="2f1f5-194">Namespace</span></span><br/>                | <span data-ttu-id="2f1f5-195">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="2f1f5-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2f1f5-196">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f1f5-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1f5-197">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="2f1f5-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="2f1f5-198">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="2f1f5-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2f1f5-199">註冊類別提供者</span><span class="sxs-lookup"><span data-stu-id="2f1f5-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="2f1f5-200">註冊執行個體提供者</span><span class="sxs-lookup"><span data-stu-id="2f1f5-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

