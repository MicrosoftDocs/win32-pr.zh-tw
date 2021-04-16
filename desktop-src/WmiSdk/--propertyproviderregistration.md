---
description: 在 WMI 中註冊屬性提供者。
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: __PropertyProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513532"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="3600a-103">\_\_PropertyProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="3600a-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="3600a-104">**\_ \_ PropertyProviderRegistration** 系統類別會在 WMI 中註冊屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="3600a-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="3600a-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3600a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3600a-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3600a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3600a-107">語法</span><span class="sxs-lookup"><span data-stu-id="3600a-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="3600a-108">成員</span><span class="sxs-lookup"><span data-stu-id="3600a-108">Members</span></span>

<span data-ttu-id="3600a-109">**\_ \_ PropertyProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3600a-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="3600a-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3600a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3600a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3600a-111">Properties</span></span>

<span data-ttu-id="3600a-112">**\_ \_ PropertyProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3600a-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3600a-113">**供應商**</span><span class="sxs-lookup"><span data-stu-id="3600a-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3600a-114">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="3600a-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="3600a-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3600a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3600a-116">[**\_ \_ 提供者**](--provider.md)實例的參考，代表屬性提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="3600a-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="3600a-117">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="3600a-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="3600a-118">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="3600a-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3600a-119">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3600a-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3600a-120">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3600a-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3600a-121">描述類別或執行個體提供者是否支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="3600a-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="3600a-122">對</span><span class="sxs-lookup"><span data-stu-id="3600a-122">True</span></span>
</dt> <dd>

<span data-ttu-id="3600a-123">提供者可透過執行 [**IWbemServices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)來支援資料抓取。</span><span class="sxs-lookup"><span data-stu-id="3600a-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="3600a-124">否</span><span class="sxs-lookup"><span data-stu-id="3600a-124">False</span></span>
</dt> <dd>

<span data-ttu-id="3600a-125">提供者不支援資料抓取，並傳回無法從 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)執行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="3600a-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3600a-126">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="3600a-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3600a-127">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3600a-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3600a-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3600a-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3600a-129">描述類別或執行個體提供者是否支援資料修改。</span><span class="sxs-lookup"><span data-stu-id="3600a-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="3600a-130">對</span><span class="sxs-lookup"><span data-stu-id="3600a-130">True</span></span>
</dt> <dd>

<span data-ttu-id="3600a-131">提供者可透過執行下列其中一種方法來支援類別或實例修改：</span><span class="sxs-lookup"><span data-stu-id="3600a-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="3600a-132">[**IWbemServices：:P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (類別提供者) </span><span class="sxs-lookup"><span data-stu-id="3600a-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="3600a-133">[**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (類別提供者) </span><span class="sxs-lookup"><span data-stu-id="3600a-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="3600a-134">否</span><span class="sxs-lookup"><span data-stu-id="3600a-134">False</span></span>
</dt> <dd>

<span data-ttu-id="3600a-135">提供者不支援資料修改，並傳回無法從 [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)或 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)進行的 **WBEM \_ E \_ 提供者 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="3600a-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3600a-136">備註</span><span class="sxs-lookup"><span data-stu-id="3600a-136">Remarks</span></span>

<span data-ttu-id="3600a-137">**\_ \_ PropertyProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="3600a-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="3600a-138">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 **\_ \_ PropertyProviderRegistration** 的實例來註冊屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="3600a-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="3600a-139">只有系統管理員可以刪除屬性提供者。</span><span class="sxs-lookup"><span data-stu-id="3600a-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="3600a-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="3600a-140">Requirements</span></span>



| <span data-ttu-id="3600a-141">需求</span><span class="sxs-lookup"><span data-stu-id="3600a-141">Requirement</span></span> | <span data-ttu-id="3600a-142">值</span><span class="sxs-lookup"><span data-stu-id="3600a-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3600a-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3600a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3600a-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3600a-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3600a-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3600a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3600a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3600a-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3600a-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="3600a-147">Namespace</span></span><br/>                | <span data-ttu-id="3600a-148">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="3600a-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3600a-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3600a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3600a-150">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="3600a-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="3600a-151">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="3600a-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3600a-152">註冊屬性提供者</span><span class="sxs-lookup"><span data-stu-id="3600a-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

