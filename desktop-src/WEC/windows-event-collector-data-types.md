---
title: 'Windows 事件收集器資料類型 (Evcoll .h) '
description: Windows 事件收集器的資料類型會用來做為事件訂閱物件變數類型、函式參數類型和函式傳回類型。
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965272"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="a6a95-105">Windows 事件收集器資料類型</span><span class="sxs-lookup"><span data-stu-id="a6a95-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="a6a95-106">Windows 事件收集器的資料類型會用來做為事件訂閱物件變數類型、函式參數類型和函式傳回類型。</span><span class="sxs-lookup"><span data-stu-id="a6a95-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="a6a95-107">**EC \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="a6a95-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6a95-108">訂用帳戶物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6a95-108">Handle to a subscription object.</span></span> <span data-ttu-id="a6a95-109">用來表示事件收集器訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="a6a95-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="a6a95-110">**EC \_ 物件 \_ 陣列 \_ 屬性 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="a6a95-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="a6a95-111">訂用帳戶之事件來源的屬性值陣列控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6a95-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="a6a95-112">當 **EcSubscriptionEventSources** 值傳遞至 *PropertyId* 參數時， [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)方法會傳回陣列控制碼。</span><span class="sxs-lookup"><span data-stu-id="a6a95-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6a95-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6a95-113">Requirements</span></span>



| <span data-ttu-id="a6a95-114">需求</span><span class="sxs-lookup"><span data-stu-id="a6a95-114">Requirement</span></span> | <span data-ttu-id="a6a95-115">值</span><span class="sxs-lookup"><span data-stu-id="a6a95-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a95-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6a95-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a95-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6a95-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="a6a95-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6a95-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a95-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6a95-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="a6a95-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a6a95-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a95-121"><dt>Evcoll。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a95-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





