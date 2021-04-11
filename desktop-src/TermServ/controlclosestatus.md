---
title: ControlCloseStatus 列舉
description: 指出包含控制項的應用程式是否可以立即關閉控制項。
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- ControlCloseStatus 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934009"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="d90a5-104">ControlCloseStatus 列舉</span><span class="sxs-lookup"><span data-stu-id="d90a5-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="d90a5-105">指出包含控制項的應用程式是否可以立即關閉控制項。</span><span class="sxs-lookup"><span data-stu-id="d90a5-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90a5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d90a5-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="d90a5-107">常數</span><span class="sxs-lookup"><span data-stu-id="d90a5-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d90a5-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span><span class="sxs-lookup"><span data-stu-id="d90a5-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="d90a5-109">容器可以立即關閉。</span><span class="sxs-lookup"><span data-stu-id="d90a5-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="d90a5-110">如果控制項未連接，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="d90a5-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="d90a5-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span><span class="sxs-lookup"><span data-stu-id="d90a5-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="d90a5-112">容器應等候事件 [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md) 或 [**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。</span><span class="sxs-lookup"><span data-stu-id="d90a5-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d90a5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d90a5-113">Requirements</span></span>



| <span data-ttu-id="d90a5-114">需求</span><span class="sxs-lookup"><span data-stu-id="d90a5-114">Requirement</span></span> | <span data-ttu-id="d90a5-115">值</span><span class="sxs-lookup"><span data-stu-id="d90a5-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d90a5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d90a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d90a5-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d90a5-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="d90a5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d90a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d90a5-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d90a5-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="d90a5-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d90a5-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d90a5-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d90a5-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d90a5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d90a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90a5-123">**IMsRdpClient::RequestClose**</span><span class="sxs-lookup"><span data-stu-id="d90a5-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="d90a5-124">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="d90a5-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="d90a5-125">**IMsTscAxEvents::OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="d90a5-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





