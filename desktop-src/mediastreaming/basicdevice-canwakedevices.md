---
title: BasicDevice. CanWakeDevices 屬性
description: 取得值，這個值會指出裝置是否可以喚醒。
ms.assetid: 0BF0B2CD-E09E-4A0B-9D48-A980CBFE4233
keywords:
- CanWakeDevices 屬性媒體串流 API
- CanWakeDevices 屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，CanWakeDevices 屬性
topic_type:
- apiref
api_name:
- BasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63fc4ed8c387c7fbe083e64311442b9e12176e5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092671"
---
# <a name="basicdevicecanwakedevices-property"></a><span data-ttu-id="3a575-106">BasicDevice. CanWakeDevices 屬性</span><span class="sxs-lookup"><span data-stu-id="3a575-106">BasicDevice.CanWakeDevices property</span></span>

<span data-ttu-id="3a575-107">取得值，這個值會指出裝置是否可以喚醒。</span><span class="sxs-lookup"><span data-stu-id="3a575-107">Gets a value that indicates if the device can wake.</span></span>

<span data-ttu-id="3a575-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="3a575-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a575-109">語法</span><span class="sxs-lookup"><span data-stu-id="3a575-109">Syntax</span></span>


```C++
HRESULT get_CanWakeDevices(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="3a575-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="3a575-110">Property value</span></span>

<span data-ttu-id="3a575-111">布林值的指標，如果裝置可以喚醒則為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="3a575-111">A pointer to a boolean value that is **True** if the device can wake.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a575-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a575-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a575-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3a575-113">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

 