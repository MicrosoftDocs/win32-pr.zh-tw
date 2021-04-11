---
description: 作為各種提供者類型之註冊類別的父類別。
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: __ProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115656"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="c9251-103">\_\_ProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="c9251-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="c9251-104">**\_ \_ ProviderRegistration** 抽象系統類別可作為各種提供者類型之註冊類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c9251-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="c9251-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c9251-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c9251-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="c9251-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9251-107">語法</span><span class="sxs-lookup"><span data-stu-id="c9251-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="c9251-108">成員</span><span class="sxs-lookup"><span data-stu-id="c9251-108">Members</span></span>

<span data-ttu-id="c9251-109">**\_ \_ ProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c9251-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c9251-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c9251-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9251-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c9251-111">Properties</span></span>

<span data-ttu-id="c9251-112">**\_ \_ ProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c9251-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9251-113">**供應商**</span><span class="sxs-lookup"><span data-stu-id="c9251-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9251-114">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="c9251-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="c9251-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c9251-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9251-116">參考 [**\_ \_ 提供**](--provider.md)者的實例，表示提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="c9251-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9251-117">備註</span><span class="sxs-lookup"><span data-stu-id="c9251-117">Remarks</span></span>

<span data-ttu-id="c9251-118">**\_ \_ ProviderRegistration** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="c9251-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="c9251-119">永遠不會建立 **\_ \_ ProviderRegistration** 系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c9251-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="c9251-120">提供者用來建立註冊實例的類別，可以直接或間接從此類別衍生。</span><span class="sxs-lookup"><span data-stu-id="c9251-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="c9251-121">這些類別是：</span><span class="sxs-lookup"><span data-stu-id="c9251-121">These classes are:</span></span>

[<span data-ttu-id="c9251-122">**\_\_ClassProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="c9251-123">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="c9251-124">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="c9251-125">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="c9251-126">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="c9251-127">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="c9251-128">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c9251-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="c9251-129">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)的實例並註冊，來註冊或刪除提供者。</span><span class="sxs-lookup"><span data-stu-id="c9251-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9251-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9251-130">Requirements</span></span>



| <span data-ttu-id="c9251-131">需求</span><span class="sxs-lookup"><span data-stu-id="c9251-131">Requirement</span></span> | <span data-ttu-id="c9251-132">值</span><span class="sxs-lookup"><span data-stu-id="c9251-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c9251-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9251-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c9251-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9251-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c9251-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9251-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c9251-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9251-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c9251-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9251-137">Namespace</span></span><br/>                | <span data-ttu-id="c9251-138">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="c9251-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c9251-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9251-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9251-140">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="c9251-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="c9251-141">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="c9251-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c9251-142">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="c9251-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

