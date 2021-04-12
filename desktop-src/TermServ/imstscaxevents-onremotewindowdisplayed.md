---
title: IMsTscAxEvents OnRemoteWindowDisplayed 方法
description: 當 RemoteApp 視窗顯示時呼叫。
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- OnRemoteWindowDisplayed 方法遠端桌面服務
- OnRemoteWindowDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteWindowDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384881"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="9e51c-106">IMsTscAxEvents：： OnRemoteWindowDisplayed 方法</span><span class="sxs-lookup"><span data-stu-id="9e51c-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="9e51c-107">當 RemoteApp 視窗顯示時呼叫。</span><span class="sxs-lookup"><span data-stu-id="9e51c-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e51c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9e51c-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="9e51c-109">參數</span><span class="sxs-lookup"><span data-stu-id="9e51c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e51c-110">*vbDisplayed* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e51c-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e51c-111">Type： **VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="9e51c-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="9e51c-112">指出是否要顯示或隱藏 RemoteApp 視窗。</span><span class="sxs-lookup"><span data-stu-id="9e51c-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="9e51c-113">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e51c-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e51c-114">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="9e51c-114">Type: **HWND**</span></span>

<span data-ttu-id="9e51c-115">視窗的控制碼隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="9e51c-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9e51c-116">*windowAttribute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9e51c-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e51c-117">類型： **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="9e51c-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="9e51c-118">[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)列舉的值，可指定事件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9e51c-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e51c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e51c-119">Return value</span></span>

<span data-ttu-id="9e51c-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9e51c-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e51c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e51c-121">Requirements</span></span>



| <span data-ttu-id="9e51c-122">需求</span><span class="sxs-lookup"><span data-stu-id="9e51c-122">Requirement</span></span> | <span data-ttu-id="9e51c-123">值</span><span class="sxs-lookup"><span data-stu-id="9e51c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e51c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e51c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9e51c-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e51c-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="9e51c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e51c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9e51c-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e51c-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="9e51c-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9e51c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e51c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e51c-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e51c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9e51c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e51c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e51c-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e51c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e51c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e51c-133">**RemoteWindowDisplayedAttribute**</span><span class="sxs-lookup"><span data-stu-id="9e51c-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="9e51c-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9e51c-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





