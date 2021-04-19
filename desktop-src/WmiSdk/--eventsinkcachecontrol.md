---
description: 用來判斷 WMI 何時釋放事件取用者提供者 IWbemUnboundObjectSink 指標。
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979349"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="1fb72-103">\_\_EventSinkCacheControl 類別</span><span class="sxs-lookup"><span data-stu-id="1fb72-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="1fb72-104">**\_ \_ EventSinkCacheControl** 系統類別用來判斷 WMI 何時釋放事件取用者提供者的 [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)指標。</span><span class="sxs-lookup"><span data-stu-id="1fb72-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="1fb72-105">**\_ \_ EventSinkCacheControl** 類別是單一類別。</span><span class="sxs-lookup"><span data-stu-id="1fb72-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="1fb72-106">它只位於 \\ 根命名空間中。</span><span class="sxs-lookup"><span data-stu-id="1fb72-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="1fb72-107">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1fb72-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1fb72-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1fb72-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb72-109">語法</span><span class="sxs-lookup"><span data-stu-id="1fb72-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="1fb72-110">成員</span><span class="sxs-lookup"><span data-stu-id="1fb72-110">Members</span></span>

<span data-ttu-id="1fb72-111">**\_ \_ EventSinkCacheControl** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1fb72-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="1fb72-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1fb72-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fb72-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1fb72-113">Properties</span></span>

<span data-ttu-id="1fb72-114">**\_ \_ EventSinkCacheControl** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1fb72-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fb72-115">**ClearAfter**</span><span class="sxs-lookup"><span data-stu-id="1fb72-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fb72-116">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1fb72-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1fb72-117">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1fb72-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1fb72-118">WMI 釋放事件提供者的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="1fb72-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="1fb72-119">這最多可能需要兩倍的間隔，以卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="1fb72-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="1fb72-120">時間是 [間隔格式](interval-format.md)。</span><span class="sxs-lookup"><span data-stu-id="1fb72-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fb72-121">備註</span><span class="sxs-lookup"><span data-stu-id="1fb72-121">Remarks</span></span>

<span data-ttu-id="1fb72-122">**\_ \_ EventSinkCacheControl** 類別衍生自 [**\_ \_ CacheControl**](--cachecontrol.md)。</span><span class="sxs-lookup"><span data-stu-id="1fb72-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="1fb72-123">如需使用這個類別的詳細資訊，請參閱卸載 [提供者](unloading-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1fb72-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb72-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fb72-124">Requirements</span></span>



| <span data-ttu-id="1fb72-125">需求</span><span class="sxs-lookup"><span data-stu-id="1fb72-125">Requirement</span></span> | <span data-ttu-id="1fb72-126">值</span><span class="sxs-lookup"><span data-stu-id="1fb72-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1fb72-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fb72-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1fb72-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1fb72-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1fb72-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fb72-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1fb72-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1fb72-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1fb72-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="1fb72-131">Namespace</span></span><br/>                | <span data-ttu-id="1fb72-132">Root</span><span class="sxs-lookup"><span data-stu-id="1fb72-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1fb72-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fb72-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb72-134">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="1fb72-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




