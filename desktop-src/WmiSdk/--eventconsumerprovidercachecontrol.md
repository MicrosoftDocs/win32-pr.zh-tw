---
description: 決定 WMI 何時應該釋放事件取用者提供者。
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981693"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="7db2f-103">\_\_EventConsumerProviderCacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="7db2f-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="7db2f-104">**\_ \_ EventConsumerProviderCacheControl** 系統類別會決定 WMI 何時應該釋放事件取用者提供者。</span><span class="sxs-lookup"><span data-stu-id="7db2f-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="7db2f-105">**\_ \_ EventConsumerProviderCacheControl** 類別是單一類別。</span><span class="sxs-lookup"><span data-stu-id="7db2f-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="7db2f-106">它只位於 \\ 根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="7db2f-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="7db2f-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="7db2f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7db2f-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="7db2f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db2f-109">語法</span><span class="sxs-lookup"><span data-stu-id="7db2f-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="7db2f-110">成員</span><span class="sxs-lookup"><span data-stu-id="7db2f-110">Members</span></span>

<span data-ttu-id="7db2f-111">**\_ \_ EventConsumerProviderCacheControl** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7db2f-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="7db2f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="7db2f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7db2f-113">屬性</span><span class="sxs-lookup"><span data-stu-id="7db2f-113">Properties</span></span>

<span data-ttu-id="7db2f-114">**\_ \_ EventConsumerProviderCacheControl** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="7db2f-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7db2f-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="7db2f-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7db2f-116">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="7db2f-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7db2f-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7db2f-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7db2f-118">WMI 釋放事件取用者提供者之前的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="7db2f-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="7db2f-119">最多可能需要指定間隔兩倍來卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="7db2f-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="7db2f-120">時間是 [間隔格式](interval-format.md)。</span><span class="sxs-lookup"><span data-stu-id="7db2f-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7db2f-121">備註</span><span class="sxs-lookup"><span data-stu-id="7db2f-121">Remarks</span></span>

<span data-ttu-id="7db2f-122">**\_ \_ EventConsumerProviderCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="7db2f-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="7db2f-123">如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="7db2f-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7db2f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="7db2f-124">Requirements</span></span>



| <span data-ttu-id="7db2f-125">需求</span><span class="sxs-lookup"><span data-stu-id="7db2f-125">Requirement</span></span> | <span data-ttu-id="7db2f-126">值</span><span class="sxs-lookup"><span data-stu-id="7db2f-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7db2f-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7db2f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7db2f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7db2f-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7db2f-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7db2f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7db2f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7db2f-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7db2f-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="7db2f-131">Namespace</span></span><br/>                | <span data-ttu-id="7db2f-132">Root</span><span class="sxs-lookup"><span data-stu-id="7db2f-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7db2f-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7db2f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db2f-134">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="7db2f-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




