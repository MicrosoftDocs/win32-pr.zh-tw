---
description: SendNMEvent 方法會將事件提交給 Windows Management Instrumentation (WMI) 。
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'IMonitorEventer：： SendNMEvent 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988679"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="7040f-103">IMonitorEventer：： SendNMEvent 方法</span><span class="sxs-lookup"><span data-stu-id="7040f-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="7040f-104">**SendNMEvent** 方法會將事件提交給 WINDOWS MANAGEMENT INSTRUMENTATION (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="7040f-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="7040f-105">語法</span><span class="sxs-lookup"><span data-stu-id="7040f-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="7040f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7040f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7040f-107">*pNMEventData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7040f-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7040f-108">提交至 WMI 的事件指標。</span><span class="sxs-lookup"><span data-stu-id="7040f-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7040f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7040f-109">Return value</span></span>

<span data-ttu-id="7040f-110">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="7040f-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="7040f-111">如果此方法不成功，傳回值就會 \_ 從記憶體中 NMERR 出來 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="7040f-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7040f-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7040f-112">Requirements</span></span>



| <span data-ttu-id="7040f-113">需求</span><span class="sxs-lookup"><span data-stu-id="7040f-113">Requirement</span></span> | <span data-ttu-id="7040f-114">值</span><span class="sxs-lookup"><span data-stu-id="7040f-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7040f-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7040f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7040f-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7040f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7040f-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7040f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7040f-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7040f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7040f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7040f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7040f-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="7040f-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




