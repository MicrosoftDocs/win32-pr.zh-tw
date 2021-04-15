---
title: 'IRemoteDesktopClientEvents OnStatusChanged 方法 (Locationapi .h) '
description: 當用戶端控制項更新其狀態時呼叫。
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- OnStatusChanged 方法遠端桌面服務
- OnStatusChanged 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnStatusChanged 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466749"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="eef75-106">IRemoteDesktopClientEvents：： OnStatusChanged 方法</span><span class="sxs-lookup"><span data-stu-id="eef75-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="eef75-107">當用戶端控制項更新其狀態時呼叫。</span><span class="sxs-lookup"><span data-stu-id="eef75-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef75-108">語法</span><span class="sxs-lookup"><span data-stu-id="eef75-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="eef75-109">參數</span><span class="sxs-lookup"><span data-stu-id="eef75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef75-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="eef75-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="eef75-111">新的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="eef75-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="eef75-112">*>statusmessage*</span><span class="sxs-lookup"><span data-stu-id="eef75-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="eef75-113">狀態訊息正文。</span><span class="sxs-lookup"><span data-stu-id="eef75-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef75-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="eef75-114">Return value</span></span>

<span data-ttu-id="eef75-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eef75-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eef75-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="eef75-116">Requirements</span></span>



| <span data-ttu-id="eef75-117">需求</span><span class="sxs-lookup"><span data-stu-id="eef75-117">Requirement</span></span> | <span data-ttu-id="eef75-118">值</span><span class="sxs-lookup"><span data-stu-id="eef75-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef75-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eef75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eef75-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eef75-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="eef75-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eef75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eef75-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eef75-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="eef75-123">標頭</span><span class="sxs-lookup"><span data-stu-id="eef75-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eef75-124"><dt>Locationapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="eef75-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="eef75-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="eef75-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="eef75-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eef75-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="eef75-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eef75-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eef75-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eef75-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="eef75-129">IID</span><span class="sxs-lookup"><span data-stu-id="eef75-129">IID</span></span><br/>                      | <span data-ttu-id="eef75-130">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="eef75-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eef75-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eef75-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef75-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="eef75-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





