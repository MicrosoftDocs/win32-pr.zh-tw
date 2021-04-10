---
description: OnFrames 方法必須由監視器所執行。 當 capture 緩衝區已滿或更新時間通過時，MCSVC 會呼叫這個方法。
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'IMonitor：： OnFrames 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690220"
---
# <a name="imonitoronframes-method"></a><span data-ttu-id="93e3a-104">IMonitor：： OnFrames 方法</span><span class="sxs-lookup"><span data-stu-id="93e3a-104">IMonitor::OnFrames method</span></span>

<span data-ttu-id="93e3a-105">**OnFrames** 方法必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="93e3a-105">The **OnFrames** method must be implemented by the monitor.</span></span> <span data-ttu-id="93e3a-106">當 capture 緩衝區已滿或更新時間通過時，MCSVC 會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="93e3a-106">The MCSVC calls this method when either the capture buffer is full or the update time has passed.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e3a-107">語法</span><span class="sxs-lookup"><span data-stu-id="93e3a-107">Syntax</span></span>


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="93e3a-108">參數</span><span class="sxs-lookup"><span data-stu-id="93e3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e3a-109">*活動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93e3a-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93e3a-110">[更新 \_](update-event.md)包含用來更新事件的框架資訊的事件結構。</span><span class="sxs-lookup"><span data-stu-id="93e3a-110">[UPDATE\_EVENT](update-event.md) structure that holds frame information used to update events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e3a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="93e3a-111">Return value</span></span>

<span data-ttu-id="93e3a-112">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同。</span><span class="sxs-lookup"><span data-stu-id="93e3a-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="93e3a-113">MCSVC 會將傳回的值傳遞回 NPP 進行處理。</span><span class="sxs-lookup"><span data-stu-id="93e3a-113">The MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="93e3a-114">如果此方法不成功，則傳回值會是錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="93e3a-114">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="93e3a-115">MCSVC 會將傳回的值傳遞回 NPP 進行處理。</span><span class="sxs-lookup"><span data-stu-id="93e3a-115">The MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e3a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="93e3a-116">Requirements</span></span>



| <span data-ttu-id="93e3a-117">需求</span><span class="sxs-lookup"><span data-stu-id="93e3a-117">Requirement</span></span> | <span data-ttu-id="93e3a-118">值</span><span class="sxs-lookup"><span data-stu-id="93e3a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93e3a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93e3a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93e3a-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e3a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="93e3a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93e3a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93e3a-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e3a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="93e3a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="93e3a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e3a-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="93e3a-124"><dt>Netmon.h</dt></span></span> </dl> |



 

 




