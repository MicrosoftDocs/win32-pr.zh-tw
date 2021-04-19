---
description: 類別是類別的抽象基類，可用來判斷 WMI 何時應該釋放元件物件模型 (COM) 物件。
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977991"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="a92a0-103">\_\_CacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="a92a0-103">\_\_CacheControl class</span></span>

<span data-ttu-id="a92a0-104">**\_ \_ CacheControl** 系統類別是類別的抽象基類，可用來判斷 WMI 何時應該釋放元件物件模型 (COM) 物件。</span><span class="sxs-lookup"><span data-stu-id="a92a0-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="a92a0-105">永遠不會建立這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a92a0-105">Instances of this class are never created.</span></span> <span data-ttu-id="a92a0-106">**\_ \_ CacheControl** 類別只位於根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="a92a0-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="a92a0-107">如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="a92a0-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="a92a0-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a92a0-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a92a0-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a92a0-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a92a0-110">語法</span><span class="sxs-lookup"><span data-stu-id="a92a0-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="a92a0-111">成員</span><span class="sxs-lookup"><span data-stu-id="a92a0-111">Members</span></span>

<span data-ttu-id="a92a0-112">**\_ \_ CacheControl** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="a92a0-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a92a0-113">備註</span><span class="sxs-lookup"><span data-stu-id="a92a0-113">Remarks</span></span>

<span data-ttu-id="a92a0-114">**\_ \_ CacheControl** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)。</span><span class="sxs-lookup"><span data-stu-id="a92a0-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a92a0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a92a0-115">Requirements</span></span>



| <span data-ttu-id="a92a0-116">需求</span><span class="sxs-lookup"><span data-stu-id="a92a0-116">Requirement</span></span> | <span data-ttu-id="a92a0-117">值</span><span class="sxs-lookup"><span data-stu-id="a92a0-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a92a0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a92a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a92a0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a92a0-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a92a0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a92a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a92a0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a92a0-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a92a0-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="a92a0-122">Namespace</span></span><br/>                | <span data-ttu-id="a92a0-123">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="a92a0-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a92a0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a92a0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a92a0-125">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="a92a0-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="a92a0-126">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="a92a0-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a92a0-127">**\_\_EventConsumerProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="a92a0-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="a92a0-128">**\_\_EventProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="a92a0-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="a92a0-129">**\_\_EventSinkCacheControl**</span><span class="sxs-lookup"><span data-stu-id="a92a0-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="a92a0-130">**\_\_ObjectProviderCacheControl**</span><span class="sxs-lookup"><span data-stu-id="a92a0-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="a92a0-131">\_\_PropertyProviderCacheControl</span><span class="sxs-lookup"><span data-stu-id="a92a0-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="a92a0-132">卸載提供者</span><span class="sxs-lookup"><span data-stu-id="a92a0-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

