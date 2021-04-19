---
description: WPD 作業 \_ 會 \_ 指出列舉值會描述正在進行之作業的目前狀態。
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: 'WPD_OPERATION_STATES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984349"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="fd1fa-103">WPD \_ 操作 \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="fd1fa-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="fd1fa-104">**WPD 作業 \_ 會 \_ 指出** 列舉值會描述正在進行之作業的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd1fa-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="fd1fa-106">常數</span><span class="sxs-lookup"><span data-stu-id="fd1fa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd1fa-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**\_未指定 WPD 作業 \_ 狀態 \_**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-108">目前的作業處於未指定的狀態 (未設定) 和未知。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD \_ 操作 \_ 狀態 \_ 已啟動**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-110">作業已啟動。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD \_ 作業 \_ 狀態 \_ 正在執行**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-112">作業正在執行。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD \_ 操作 \_ 狀態已 \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-114">作業已暫停。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD \_ 操作 \_ 狀態已 \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-116">作業已取消。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD \_ 操作 \_ 狀態 \_ 已完成**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-118">作業已完成。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="fd1fa-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD \_ 操作 \_ 狀態已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="fd1fa-120">作業已中止。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd1fa-121">備註</span><span class="sxs-lookup"><span data-stu-id="fd1fa-121">Remarks</span></span>

<span data-ttu-id="fd1fa-122">這些值會在應用程式定義的回呼中收到 ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)) 。</span><span class="sxs-lookup"><span data-stu-id="fd1fa-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1fa-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd1fa-123">Requirements</span></span>



| <span data-ttu-id="fd1fa-124">需求</span><span class="sxs-lookup"><span data-stu-id="fd1fa-124">Requirement</span></span> | <span data-ttu-id="fd1fa-125">值</span><span class="sxs-lookup"><span data-stu-id="fd1fa-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1fa-126">標頭</span><span class="sxs-lookup"><span data-stu-id="fd1fa-126">Header</span></span><br/> | <dl> <span data-ttu-id="fd1fa-127"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1fa-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1fa-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd1fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1fa-129">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="fd1fa-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




