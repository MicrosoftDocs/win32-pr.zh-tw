---
description: 控制何時卸載類別或執行個體提供者。
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: __ObjectProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985336"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="124af-103">\_\_ObjectProviderCacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="124af-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="124af-104">**\_ \_ ObjectProviderCacheControl** 系統類別會控制何時卸載類別或執行個體提供者。</span><span class="sxs-lookup"><span data-stu-id="124af-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="124af-105">它只位於 \\ 根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="124af-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="124af-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="124af-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="124af-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="124af-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="124af-108">語法</span><span class="sxs-lookup"><span data-stu-id="124af-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="124af-109">成員</span><span class="sxs-lookup"><span data-stu-id="124af-109">Members</span></span>

<span data-ttu-id="124af-110">**\_ \_ ObjectProviderCacheControl** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="124af-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="124af-111">屬性</span><span class="sxs-lookup"><span data-stu-id="124af-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="124af-112">屬性</span><span class="sxs-lookup"><span data-stu-id="124af-112">Properties</span></span>

<span data-ttu-id="124af-113">**\_ \_ ObjectProviderCacheControl** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="124af-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="124af-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="124af-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="124af-115">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="124af-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="124af-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="124af-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="124af-117">WMI 釋放實例、類別或方法提供者之前的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="124af-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="124af-118">時間是 [間隔格式](interval-format.md)。</span><span class="sxs-lookup"><span data-stu-id="124af-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="124af-119">備註</span><span class="sxs-lookup"><span data-stu-id="124af-119">Remarks</span></span>

<span data-ttu-id="124af-120">**\_ \_ ObjectProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="124af-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="124af-121">如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="124af-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="124af-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="124af-122">Requirements</span></span>



| <span data-ttu-id="124af-123">需求</span><span class="sxs-lookup"><span data-stu-id="124af-123">Requirement</span></span> | <span data-ttu-id="124af-124">值</span><span class="sxs-lookup"><span data-stu-id="124af-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="124af-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="124af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="124af-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="124af-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="124af-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="124af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="124af-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="124af-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="124af-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="124af-129">Namespace</span></span><br/>                | <span data-ttu-id="124af-130">Root</span><span class="sxs-lookup"><span data-stu-id="124af-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="124af-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="124af-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124af-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="124af-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="124af-133">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="124af-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="124af-134">隨時接收事件</span><span class="sxs-lookup"><span data-stu-id="124af-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

