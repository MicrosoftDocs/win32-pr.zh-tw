---
title: IRemoteDesktopClientEvents OnTouchPointerCursorMoved 方法
description: 當觸控指標游標已移動，且 EventsEnabled 屬性設定為 true 時呼叫。
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- OnTouchPointerCursorMoved 方法遠端桌面服務
- OnTouchPointerCursorMoved 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnTouchPointerCursorMoved 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965902"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="630df-106">IRemoteDesktopClientEvents：： OnTouchPointerCursorMoved 方法</span><span class="sxs-lookup"><span data-stu-id="630df-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="630df-107">當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。</span><span class="sxs-lookup"><span data-stu-id="630df-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="630df-108">語法</span><span class="sxs-lookup"><span data-stu-id="630df-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="630df-109">參數</span><span class="sxs-lookup"><span data-stu-id="630df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="630df-110">*x* \[ 于\]</span><span class="sxs-lookup"><span data-stu-id="630df-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="630df-111">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="630df-111">*y* \[in\]</span></span>
<span data-ttu-id="630df-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="630df-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="630df-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="630df-113">Return value</span></span>

<span data-ttu-id="630df-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="630df-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="630df-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="630df-115">Requirements</span></span>



| <span data-ttu-id="630df-116">需求</span><span class="sxs-lookup"><span data-stu-id="630df-116">Requirement</span></span> | <span data-ttu-id="630df-117">值</span><span class="sxs-lookup"><span data-stu-id="630df-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="630df-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="630df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="630df-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="630df-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="630df-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="630df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="630df-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="630df-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="630df-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="630df-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="630df-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630df-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="630df-124">DLL</span><span class="sxs-lookup"><span data-stu-id="630df-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630df-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630df-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="630df-126">IID</span><span class="sxs-lookup"><span data-stu-id="630df-126">IID</span></span><br/>                      | <span data-ttu-id="630df-127">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="630df-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="630df-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="630df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630df-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="630df-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

