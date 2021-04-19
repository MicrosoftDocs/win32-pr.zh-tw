---
description: 用來向 Windows Management Instrumentation (WMI) 註冊事件提供者。
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994385"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="a0103-103">\_\_EventProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="a0103-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="a0103-104">**\_ \_ EventProviderRegistration** 系統類別可用來向 Windows Management Instrumentation (WMI) 註冊事件提供者。</span><span class="sxs-lookup"><span data-stu-id="a0103-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="a0103-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a0103-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a0103-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a0103-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0103-107">語法</span><span class="sxs-lookup"><span data-stu-id="a0103-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="a0103-108">成員</span><span class="sxs-lookup"><span data-stu-id="a0103-108">Members</span></span>

<span data-ttu-id="a0103-109">**\_ \_ EventProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a0103-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="a0103-110">屬性</span><span class="sxs-lookup"><span data-stu-id="a0103-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0103-111">屬性</span><span class="sxs-lookup"><span data-stu-id="a0103-111">Properties</span></span>

<span data-ttu-id="a0103-112">**\_ \_ EventProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a0103-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0103-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="a0103-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0103-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="a0103-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a0103-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a0103-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a0103-116">一或多個 Windows Management Instrumentation 查詢語言 (WQL) 查詢，描述事件提供者所支援的事件。</span><span class="sxs-lookup"><span data-stu-id="a0103-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="a0103-117">**供應商**</span><span class="sxs-lookup"><span data-stu-id="a0103-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0103-118">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="a0103-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="a0103-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a0103-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0103-120">事件提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="a0103-120">Object path to the event provider.</span></span> <span data-ttu-id="a0103-121">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="a0103-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0103-122">備註</span><span class="sxs-lookup"><span data-stu-id="a0103-122">Remarks</span></span>

<span data-ttu-id="a0103-123">只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md)的實例，來註冊或刪除事件提供者。</span><span class="sxs-lookup"><span data-stu-id="a0103-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="a0103-124">**\_ \_ EventProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="a0103-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0103-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0103-125">Requirements</span></span>



| <span data-ttu-id="a0103-126">需求</span><span class="sxs-lookup"><span data-stu-id="a0103-126">Requirement</span></span> | <span data-ttu-id="a0103-127">值</span><span class="sxs-lookup"><span data-stu-id="a0103-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a0103-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0103-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a0103-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0103-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a0103-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0103-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a0103-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0103-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a0103-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0103-132">Namespace</span></span><br/>                | <span data-ttu-id="a0103-133">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a0103-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a0103-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0103-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0103-135">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="a0103-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="a0103-136">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="a0103-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a0103-137">註冊事件提供者</span><span class="sxs-lookup"><span data-stu-id="a0103-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="a0103-138">撰寫事件提供者</span><span class="sxs-lookup"><span data-stu-id="a0103-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

