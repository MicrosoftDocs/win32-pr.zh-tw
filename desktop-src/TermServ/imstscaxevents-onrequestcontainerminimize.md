---
title: IMsTscAxEvents OnRequestContainerMinimize 方法
description: 當使用者在全螢幕模式下的連接列上按下最小化按鈕時呼叫。 引發此事件是容器應用程式本身最小化的要求。
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- OnRequestContainerMinimize 方法遠端桌面服務
- OnRequestContainerMinimize 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRequestContainerMinimize 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85387e3b156eed29dc7068eac84280be521a934e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384878"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a><span data-ttu-id="ed14a-107">IMsTscAxEvents：： OnRequestContainerMinimize 方法</span><span class="sxs-lookup"><span data-stu-id="ed14a-107">IMsTscAxEvents::OnRequestContainerMinimize method</span></span>

<span data-ttu-id="ed14a-108">當使用者在全螢幕模式下的連接列上按下 **最小化** 按鈕時呼叫。</span><span class="sxs-lookup"><span data-stu-id="ed14a-108">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="ed14a-109">引發此事件是容器應用程式本身最小化的要求。</span><span class="sxs-lookup"><span data-stu-id="ed14a-109">The firing of this event is a request that the container application minimize itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed14a-110">語法</span><span class="sxs-lookup"><span data-stu-id="ed14a-110">Syntax</span></span>


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a><span data-ttu-id="ed14a-111">參數</span><span class="sxs-lookup"><span data-stu-id="ed14a-111">Parameters</span></span>

<span data-ttu-id="ed14a-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ed14a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed14a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed14a-113">Return value</span></span>

<span data-ttu-id="ed14a-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ed14a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed14a-115">備註</span><span class="sxs-lookup"><span data-stu-id="ed14a-115">Remarks</span></span>

<span data-ttu-id="ed14a-116">只有在已啟用容器處理的全螢幕模式時，才會呼叫這個方法。如需詳細資訊，請參閱 [**IMsTscAdvancedSettings：:p 的 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 。</span><span class="sxs-lookup"><span data-stu-id="ed14a-116">This method will only be called if the container-handled full-screen mode is enabled - see [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed14a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed14a-117">Requirements</span></span>



| <span data-ttu-id="ed14a-118">需求</span><span class="sxs-lookup"><span data-stu-id="ed14a-118">Requirement</span></span> | <span data-ttu-id="ed14a-119">值</span><span class="sxs-lookup"><span data-stu-id="ed14a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed14a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed14a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed14a-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed14a-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ed14a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed14a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed14a-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed14a-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ed14a-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ed14a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed14a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed14a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ed14a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ed14a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed14a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed14a-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ed14a-128">IID</span><span class="sxs-lookup"><span data-stu-id="ed14a-128">IID</span></span><br/>                      | <span data-ttu-id="ed14a-129">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ed14a-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ed14a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed14a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed14a-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ed14a-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





