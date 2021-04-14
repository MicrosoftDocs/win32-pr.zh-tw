---
description: 控制何時卸載事件提供者。
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193648"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="94a73-103">\_\_EventProviderCacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="94a73-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="94a73-104">**\_ \_ EventProviderCacheControl** 系統類別會控制何時卸載事件提供者。</span><span class="sxs-lookup"><span data-stu-id="94a73-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="94a73-105">它只位於 \\ 根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="94a73-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="94a73-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="94a73-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="94a73-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="94a73-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a73-108">語法</span><span class="sxs-lookup"><span data-stu-id="94a73-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="94a73-109">成員</span><span class="sxs-lookup"><span data-stu-id="94a73-109">Members</span></span>

<span data-ttu-id="94a73-110">**\_ \_ EventProviderCacheControl** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="94a73-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="94a73-111">屬性</span><span class="sxs-lookup"><span data-stu-id="94a73-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94a73-112">屬性</span><span class="sxs-lookup"><span data-stu-id="94a73-112">Properties</span></span>

<span data-ttu-id="94a73-113">**\_ \_ EventProviderCacheControl** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="94a73-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94a73-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="94a73-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94a73-115">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="94a73-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="94a73-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="94a73-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="94a73-117">Windows Management Instrumentation (WMI) 釋放事件提供者之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="94a73-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="94a73-118">時間是 [間隔格式](interval-format.md)。</span><span class="sxs-lookup"><span data-stu-id="94a73-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="94a73-119">最多可能需要指定間隔兩倍來卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="94a73-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94a73-120">備註</span><span class="sxs-lookup"><span data-stu-id="94a73-120">Remarks</span></span>

<span data-ttu-id="94a73-121">**\_ \_ EventProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="94a73-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="94a73-122">如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="94a73-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94a73-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="94a73-123">Requirements</span></span>



| <span data-ttu-id="94a73-124">需求</span><span class="sxs-lookup"><span data-stu-id="94a73-124">Requirement</span></span> | <span data-ttu-id="94a73-125">值</span><span class="sxs-lookup"><span data-stu-id="94a73-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94a73-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94a73-126">Minimum supported client</span></span><br/> | <span data-ttu-id="94a73-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94a73-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94a73-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94a73-128">Minimum supported server</span></span><br/> | <span data-ttu-id="94a73-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94a73-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="94a73-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="94a73-130">Namespace</span></span><br/>                | <span data-ttu-id="94a73-131">Root</span><span class="sxs-lookup"><span data-stu-id="94a73-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="94a73-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94a73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a73-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="94a73-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="94a73-134">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="94a73-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

