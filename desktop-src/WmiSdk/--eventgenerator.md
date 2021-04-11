---
description: 作為控制事件產生（例如計時器事件）之類別的父類別。
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195401"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="70cc5-103">\_\_EventGenerator 類別</span><span class="sxs-lookup"><span data-stu-id="70cc5-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="70cc5-104">**\_ \_ EventGenerator** 系統類別是抽象基類，可作為控制事件產生（例如 [計時器事件](receiving-a-timed-or-repeating-event.md)）之類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="70cc5-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="70cc5-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="70cc5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="70cc5-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="70cc5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="70cc5-107">語法</span><span class="sxs-lookup"><span data-stu-id="70cc5-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="70cc5-108">成員</span><span class="sxs-lookup"><span data-stu-id="70cc5-108">Members</span></span>

<span data-ttu-id="70cc5-109">**\_ \_ EventGenerator** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="70cc5-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="70cc5-110">備註</span><span class="sxs-lookup"><span data-stu-id="70cc5-110">Remarks</span></span>

<span data-ttu-id="70cc5-111">**\_ \_ EventGenerator** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="70cc5-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="70cc5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="70cc5-112">Requirements</span></span>



| <span data-ttu-id="70cc5-113">需求</span><span class="sxs-lookup"><span data-stu-id="70cc5-113">Requirement</span></span> | <span data-ttu-id="70cc5-114">值</span><span class="sxs-lookup"><span data-stu-id="70cc5-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="70cc5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70cc5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70cc5-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70cc5-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="70cc5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70cc5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70cc5-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70cc5-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="70cc5-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="70cc5-119">Namespace</span></span><br/>                | <span data-ttu-id="70cc5-120">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="70cc5-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="70cc5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70cc5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70cc5-122">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="70cc5-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="70cc5-123">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="70cc5-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

