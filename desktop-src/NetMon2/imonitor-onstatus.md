---
description: MCSVC 方法會呼叫 OnStatus 方法，以通知監視器有 NPP 狀態事件存在。 此方法必須由監視器所執行。
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'IMonitor：： OnStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114145"
---
# <a name="imonitoronstatus-method"></a><span data-ttu-id="32ac7-104">IMonitor：： OnStatus 方法</span><span class="sxs-lookup"><span data-stu-id="32ac7-104">IMonitor::OnStatus method</span></span>

<span data-ttu-id="32ac7-105">MCSVC 方法會呼叫 **OnStatus** 方法，以通知監視器有 NPP 狀態事件存在。</span><span class="sxs-lookup"><span data-stu-id="32ac7-105">The MCSVC method calls the **OnStatus** method to notify the monitor that an NPP status event exists.</span></span> <span data-ttu-id="32ac7-106">此方法必須由監視器所執行。</span><span class="sxs-lookup"><span data-stu-id="32ac7-106">This method must be implemented by the monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ac7-107">語法</span><span class="sxs-lookup"><span data-stu-id="32ac7-107">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a><span data-ttu-id="32ac7-108">參數</span><span class="sxs-lookup"><span data-stu-id="32ac7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ac7-109">*活動* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32ac7-109">*Event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ac7-110">[UPDATE \_ 事件](update-event.md)結構。</span><span class="sxs-lookup"><span data-stu-id="32ac7-110">An [UPDATE\_EVENT](update-event.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ac7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="32ac7-111">Return value</span></span>

<span data-ttu-id="32ac7-112">如果方法成功，則傳回值為 S \_ OK (與 >aad-userreadusingalternativesecurityid-noerror) 相同，而且 MCSVC 會將傳回的值傳回到 NPP 進行處理。</span><span class="sxs-lookup"><span data-stu-id="32ac7-112">If the method is successful, the return value is S\_OK (which is the same as NOERROR), and the MCSVC passes the returned value back to the NPP for processing.</span></span>

<span data-ttu-id="32ac7-113">如果方法失敗，則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="32ac7-113">If the method is unsuccessful, return an error code.</span></span> <span data-ttu-id="32ac7-114">發生錯誤時，MCSVC 會將傳回的值傳遞回 NPP 進行處理。</span><span class="sxs-lookup"><span data-stu-id="32ac7-114">On error, the MCSVC passes the returned value back to the NPP for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ac7-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="32ac7-115">Requirements</span></span>



| <span data-ttu-id="32ac7-116">需求</span><span class="sxs-lookup"><span data-stu-id="32ac7-116">Requirement</span></span> | <span data-ttu-id="32ac7-117">值</span><span class="sxs-lookup"><span data-stu-id="32ac7-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32ac7-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32ac7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32ac7-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32ac7-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="32ac7-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32ac7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32ac7-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32ac7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="32ac7-122">標頭</span><span class="sxs-lookup"><span data-stu-id="32ac7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ac7-123"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="32ac7-123"><dt>Netmon.h</dt></span></span> </dl> |



 

 




