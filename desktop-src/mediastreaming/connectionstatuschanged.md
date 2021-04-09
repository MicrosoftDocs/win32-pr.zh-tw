---
title: ConnectionStatusChanged 事件
description: 發生于裝置的網路連接狀態變更時。
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- ConnectionStatusChanged 事件媒體串流 API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682223"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="330cc-104">ConnectionStatusChanged 事件</span><span class="sxs-lookup"><span data-stu-id="330cc-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="330cc-105">發生于裝置的網路連接狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="330cc-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="330cc-106">語法</span><span class="sxs-lookup"><span data-stu-id="330cc-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="330cc-107">參數</span><span class="sxs-lookup"><span data-stu-id="330cc-107">Parameters</span></span>

<span data-ttu-id="330cc-108">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="330cc-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="330cc-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="330cc-109">Return value</span></span>

<span data-ttu-id="330cc-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="330cc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="330cc-111">備註</span><span class="sxs-lookup"><span data-stu-id="330cc-111">Remarks</span></span>

<span data-ttu-id="330cc-112">若要處理此事件的通知，請使用 [**add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)方法來註冊 [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))事件處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="330cc-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="330cc-113">若要取消註冊事件處理常式，請使用 [**remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="330cc-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 