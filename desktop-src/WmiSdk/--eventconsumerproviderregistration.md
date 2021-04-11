---
description: 向 WMI 註冊事件取用者提供者。
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851240"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="67f33-103">\_\_EventConsumerProviderRegistration 類別</span><span class="sxs-lookup"><span data-stu-id="67f33-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="67f33-104">**\_ \_ EventConsumerProviderRegistration** 系統類別會向 WMI 註冊事件取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="67f33-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="67f33-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="67f33-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="67f33-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="67f33-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f33-107">語法</span><span class="sxs-lookup"><span data-stu-id="67f33-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="67f33-108">成員</span><span class="sxs-lookup"><span data-stu-id="67f33-108">Members</span></span>

<span data-ttu-id="67f33-109">**\_ \_ EventConsumerProviderRegistration** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67f33-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="67f33-110">屬性</span><span class="sxs-lookup"><span data-stu-id="67f33-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67f33-111">屬性</span><span class="sxs-lookup"><span data-stu-id="67f33-111">Properties</span></span>

<span data-ttu-id="67f33-112">**\_ \_ EventConsumerProviderRegistration** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="67f33-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67f33-113">**ConsumerClassNames**</span><span class="sxs-lookup"><span data-stu-id="67f33-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f33-114">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="67f33-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67f33-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="67f33-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="67f33-116">事件取用者提供者所支援之邏輯取用者類別的名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="67f33-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="67f33-117">**供應商**</span><span class="sxs-lookup"><span data-stu-id="67f33-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67f33-118">資料類型： **\_ \_ 提供者**</span><span class="sxs-lookup"><span data-stu-id="67f33-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="67f33-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="67f33-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67f33-120">提供者的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="67f33-120">Object path to the provider.</span></span> <span data-ttu-id="67f33-121">這個屬性繼承自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="67f33-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67f33-122">備註</span><span class="sxs-lookup"><span data-stu-id="67f33-122">Remarks</span></span>

<span data-ttu-id="67f33-123">**\_ \_ EventConsumerProviderRegistration** 類別衍生自 [**\_ \_ ProviderRegistration**](--providerregistration.md)。</span><span class="sxs-lookup"><span data-stu-id="67f33-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67f33-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="67f33-124">Requirements</span></span>



| <span data-ttu-id="67f33-125">需求</span><span class="sxs-lookup"><span data-stu-id="67f33-125">Requirement</span></span> | <span data-ttu-id="67f33-126">值</span><span class="sxs-lookup"><span data-stu-id="67f33-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="67f33-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67f33-127">Minimum supported client</span></span><br/> | <span data-ttu-id="67f33-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67f33-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="67f33-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67f33-129">Minimum supported server</span></span><br/> | <span data-ttu-id="67f33-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67f33-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="67f33-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="67f33-131">Namespace</span></span><br/>                | <span data-ttu-id="67f33-132">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="67f33-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="67f33-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67f33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f33-134">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="67f33-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="67f33-135">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="67f33-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="67f33-136">註冊事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="67f33-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="67f33-137">撰寫事件取用者提供者</span><span class="sxs-lookup"><span data-stu-id="67f33-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

