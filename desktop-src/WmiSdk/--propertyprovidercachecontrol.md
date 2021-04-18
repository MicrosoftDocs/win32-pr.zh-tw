---
description: 當卸載屬性提供者時，控制快取。
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193068"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="3822b-103">\_\_PropertyProviderCacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="3822b-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="3822b-104">當卸載屬性提供者時， **\_ \_ PropertyProviderCacheControl** 類別會控制快取。</span><span class="sxs-lookup"><span data-stu-id="3822b-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="3822b-105">這個類別只存在於 \\ 根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="3822b-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="3822b-106">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3822b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3822b-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="3822b-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3822b-108">語法</span><span class="sxs-lookup"><span data-stu-id="3822b-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="3822b-109">成員</span><span class="sxs-lookup"><span data-stu-id="3822b-109">Members</span></span>

<span data-ttu-id="3822b-110">**\_ \_ PropertyProviderCacheControl** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3822b-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="3822b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3822b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3822b-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3822b-112">Properties</span></span>

<span data-ttu-id="3822b-113">**\_ \_ PropertyProviderCacheControl** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3822b-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3822b-114">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="3822b-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3822b-115">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3822b-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3822b-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3822b-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3822b-117">WMI 釋放屬性提供者之後的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="3822b-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="3822b-118">時間是間隔格式。</span><span class="sxs-lookup"><span data-stu-id="3822b-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3822b-119">備註</span><span class="sxs-lookup"><span data-stu-id="3822b-119">Remarks</span></span>

<span data-ttu-id="3822b-120">**\_ \_ PropertyProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="3822b-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="3822b-121">如需詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3822b-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3822b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3822b-122">Requirements</span></span>



| <span data-ttu-id="3822b-123">需求</span><span class="sxs-lookup"><span data-stu-id="3822b-123">Requirement</span></span> | <span data-ttu-id="3822b-124">值</span><span class="sxs-lookup"><span data-stu-id="3822b-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3822b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3822b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3822b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3822b-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3822b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3822b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3822b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3822b-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3822b-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="3822b-129">Namespace</span></span><br/>                | <span data-ttu-id="3822b-130">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="3822b-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3822b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3822b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3822b-132">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="3822b-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




