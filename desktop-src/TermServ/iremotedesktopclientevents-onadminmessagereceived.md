---
title: IRemoteDesktopClientEvents OnAdminMessageReceived 方法
description: 當用戶端控制項收到系統管理訊息時呼叫。
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- OnAdminMessageReceived 方法遠端桌面服務
- OnAdminMessageReceived 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnAdminMessageReceived 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384977"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="8bc52-106">IRemoteDesktopClientEvents：： OnAdminMessageReceived 方法</span><span class="sxs-lookup"><span data-stu-id="8bc52-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="8bc52-107">當用戶端控制項收到系統管理訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="8bc52-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc52-108">語法</span><span class="sxs-lookup"><span data-stu-id="8bc52-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="8bc52-109">參數</span><span class="sxs-lookup"><span data-stu-id="8bc52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc52-110">*adminMessage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8bc52-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc52-111">訊息。</span><span class="sxs-lookup"><span data-stu-id="8bc52-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc52-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bc52-112">Return value</span></span>

<span data-ttu-id="8bc52-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8bc52-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc52-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bc52-114">Requirements</span></span>



| <span data-ttu-id="8bc52-115">需求</span><span class="sxs-lookup"><span data-stu-id="8bc52-115">Requirement</span></span> | <span data-ttu-id="8bc52-116">值</span><span class="sxs-lookup"><span data-stu-id="8bc52-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc52-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bc52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8bc52-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8bc52-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="8bc52-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bc52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8bc52-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8bc52-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="8bc52-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8bc52-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8bc52-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bc52-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="8bc52-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8bc52-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bc52-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bc52-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="8bc52-125">IID</span><span class="sxs-lookup"><span data-stu-id="8bc52-125">IID</span></span><br/>                      | <span data-ttu-id="8bc52-126">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="8bc52-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bc52-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bc52-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc52-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="8bc52-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





