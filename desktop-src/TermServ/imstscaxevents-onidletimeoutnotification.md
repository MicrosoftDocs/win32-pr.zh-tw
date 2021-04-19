---
title: IMsTscAxEvents OnIdleTimeoutNotification 方法
description: 當使用者在 IMsRdpClientAdvancedSettings put MinutesToIdleTimeout 方法所設定的一段時間內沒有滑鼠或鍵盤輸入時呼叫 \_ 。
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- OnIdleTimeoutNotification 方法遠端桌面服務
- OnIdleTimeoutNotification 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnIdleTimeoutNotification 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969595"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="e82f4-106">IMsTscAxEvents：： OnIdleTimeoutNotification 方法</span><span class="sxs-lookup"><span data-stu-id="e82f4-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="e82f4-107">當使用者在 [**IMsRdpClientAdvancedSettings：:p 長 \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 方法設定期間沒有滑鼠或鍵盤輸入時呼叫。</span><span class="sxs-lookup"><span data-stu-id="e82f4-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82f4-108">語法</span><span class="sxs-lookup"><span data-stu-id="e82f4-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="e82f4-109">參數</span><span class="sxs-lookup"><span data-stu-id="e82f4-109">Parameters</span></span>

<span data-ttu-id="e82f4-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e82f4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e82f4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e82f4-111">Return value</span></span>

<span data-ttu-id="e82f4-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e82f4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e82f4-113">備註</span><span class="sxs-lookup"><span data-stu-id="e82f4-113">Remarks</span></span>

<span data-ttu-id="e82f4-114">根據預設， [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 屬性的值會設定為零，而且系統不會監視閒置時間。</span><span class="sxs-lookup"><span data-stu-id="e82f4-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="e82f4-115">只有當屬性設定為非零值時，才會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="e82f4-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="e82f4-116">每次發生事件時，就會自動重設 [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="e82f4-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="e82f4-117">應用程式在中斷使用者的連線時，可以使用 [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) ;例如，在 kiosk 或其他公用終端機案例中。</span><span class="sxs-lookup"><span data-stu-id="e82f4-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="e82f4-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e82f4-118">Requirements</span></span>



| <span data-ttu-id="e82f4-119">需求</span><span class="sxs-lookup"><span data-stu-id="e82f4-119">Requirement</span></span> | <span data-ttu-id="e82f4-120">值</span><span class="sxs-lookup"><span data-stu-id="e82f4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e82f4-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e82f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e82f4-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e82f4-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e82f4-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e82f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e82f4-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e82f4-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e82f4-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e82f4-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e82f4-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82f4-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e82f4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e82f4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e82f4-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82f4-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e82f4-129">IID</span><span class="sxs-lookup"><span data-stu-id="e82f4-129">IID</span></span><br/>                      | <span data-ttu-id="e82f4-130">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e82f4-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e82f4-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e82f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82f4-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e82f4-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





