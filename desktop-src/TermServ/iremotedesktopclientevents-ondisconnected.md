---
title: IRemoteDesktopClientEvents OnDisconnected 方法
description: 當用戶端控制項與遠端會話中斷連接時呼叫。
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- OnDisconnected 方法遠端桌面服務
- OnDisconnected 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnDisconnected 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686128"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="28597-106">IRemoteDesktopClientEvents：： OnDisconnected 方法</span><span class="sxs-lookup"><span data-stu-id="28597-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="28597-107">當用戶端控制項與遠端會話中斷連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="28597-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="28597-108">語法</span><span class="sxs-lookup"><span data-stu-id="28597-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="28597-109">參數</span><span class="sxs-lookup"><span data-stu-id="28597-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28597-110">*disconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28597-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28597-111">中斷線上活動的原因。</span><span class="sxs-lookup"><span data-stu-id="28597-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="28597-112">*ExtendedDisconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28597-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28597-113">中斷線上活動的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="28597-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="28597-114">*disconnectErrorMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28597-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28597-115">中斷線上活動的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="28597-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28597-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="28597-116">Return value</span></span>

<span data-ttu-id="28597-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="28597-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28597-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="28597-118">Requirements</span></span>



| <span data-ttu-id="28597-119">需求</span><span class="sxs-lookup"><span data-stu-id="28597-119">Requirement</span></span> | <span data-ttu-id="28597-120">值</span><span class="sxs-lookup"><span data-stu-id="28597-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28597-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28597-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28597-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="28597-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="28597-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28597-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28597-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28597-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="28597-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="28597-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="28597-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28597-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="28597-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28597-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28597-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28597-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="28597-129">IID</span><span class="sxs-lookup"><span data-stu-id="28597-129">IID</span></span><br/>                      | <span data-ttu-id="28597-130">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="28597-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28597-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28597-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28597-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="28597-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





