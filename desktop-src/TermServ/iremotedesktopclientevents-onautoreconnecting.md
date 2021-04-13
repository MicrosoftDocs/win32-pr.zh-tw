---
title: IRemoteDesktopClientEvents OnAutoReconnecting 方法
description: 當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- OnAutoReconnecting 方法遠端桌面服務
- OnAutoReconnecting 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnAutoReconnecting 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509395"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="17fd7-106">IRemoteDesktopClientEvents：： OnAutoReconnecting 方法</span><span class="sxs-lookup"><span data-stu-id="17fd7-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="17fd7-107">當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="17fd7-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fd7-108">語法</span><span class="sxs-lookup"><span data-stu-id="17fd7-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="17fd7-109">參數</span><span class="sxs-lookup"><span data-stu-id="17fd7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17fd7-110">*disconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-111">中斷線上活動的原因。</span><span class="sxs-lookup"><span data-stu-id="17fd7-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="17fd7-112">*ExtendedDisconnectReason* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-113">中斷線上活動的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="17fd7-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="17fd7-114">*disconnectErrorMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-115">中斷線上活動的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="17fd7-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="17fd7-116">*networkAvailable* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-117">網路是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="17fd7-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="17fd7-118">*了 attemptcount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-119">這會嘗試這麼做。</span><span class="sxs-lookup"><span data-stu-id="17fd7-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="17fd7-120">*maxAttemptCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17fd7-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17fd7-121">將會執行重新連線嘗試的次數上限。</span><span class="sxs-lookup"><span data-stu-id="17fd7-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17fd7-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="17fd7-122">Return value</span></span>

<span data-ttu-id="17fd7-123">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="17fd7-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="17fd7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="17fd7-124">Requirements</span></span>



| <span data-ttu-id="17fd7-125">需求</span><span class="sxs-lookup"><span data-stu-id="17fd7-125">Requirement</span></span> | <span data-ttu-id="17fd7-126">值</span><span class="sxs-lookup"><span data-stu-id="17fd7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17fd7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17fd7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="17fd7-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="17fd7-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="17fd7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17fd7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="17fd7-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="17fd7-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="17fd7-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="17fd7-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="17fd7-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fd7-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="17fd7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="17fd7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17fd7-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17fd7-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="17fd7-135">IID</span><span class="sxs-lookup"><span data-stu-id="17fd7-135">IID</span></span><br/>                      | <span data-ttu-id="17fd7-136">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="17fd7-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17fd7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17fd7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17fd7-138">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="17fd7-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





