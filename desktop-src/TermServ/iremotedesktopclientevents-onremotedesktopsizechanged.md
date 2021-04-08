---
title: IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged 方法
description: 當遠端桌面大小變更時呼叫。
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- OnRemoteDesktopSizeChanged 方法遠端桌面服務
- OnRemoteDesktopSizeChanged 方法遠端桌面服務，IRemoteDesktopClientEvents 介面
- IRemoteDesktopClientEvents 介面遠端桌面服務，OnRemoteDesktopSizeChanged 方法
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685862"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="fd848-106">IRemoteDesktopClientEvents：： OnRemoteDesktopSizeChanged 方法</span><span class="sxs-lookup"><span data-stu-id="fd848-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="fd848-107">當遠端桌面大小變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fd848-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd848-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd848-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="fd848-109">參數</span><span class="sxs-lookup"><span data-stu-id="fd848-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd848-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd848-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd848-111">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd848-111">*height* \[in\]</span></span>
<span data-ttu-id="fd848-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd848-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="fd848-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd848-113">Return value</span></span>

<span data-ttu-id="fd848-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="fd848-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd848-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd848-115">Requirements</span></span>



| <span data-ttu-id="fd848-116">需求</span><span class="sxs-lookup"><span data-stu-id="fd848-116">Requirement</span></span> | <span data-ttu-id="fd848-117">值</span><span class="sxs-lookup"><span data-stu-id="fd848-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd848-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd848-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fd848-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fd848-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="fd848-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd848-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fd848-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd848-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="fd848-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fd848-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd848-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd848-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fd848-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fd848-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd848-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd848-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fd848-126">IID</span><span class="sxs-lookup"><span data-stu-id="fd848-126">IID</span></span><br/>                      | <span data-ttu-id="fd848-127">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="fd848-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd848-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd848-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd848-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="fd848-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





