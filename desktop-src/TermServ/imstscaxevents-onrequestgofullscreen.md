---
title: IMsTscAxEvents OnRequestGoFullScreen 方法
description: 當用戶端要求切換至全螢幕模式並呼叫 IMsTscAdvancedSettings put \_ ContainerHandledFullScreen 方法以將 ContainerHandledFullScreen 屬性設定為非零值時呼叫。
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- OnRequestGoFullScreen 方法遠端桌面服務
- OnRequestGoFullScreen 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRequestGoFullScreen 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384877"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="19421-106">IMsTscAxEvents：： OnRequestGoFullScreen 方法</span><span class="sxs-lookup"><span data-stu-id="19421-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="19421-107">當用戶端要求切換至全螢幕模式並呼叫 [**IMsTscAdvancedSettings：:p 使用 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 方法時呼叫，以將 **ContainerHandledFullScreen** 屬性設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="19421-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="19421-108">語法</span><span class="sxs-lookup"><span data-stu-id="19421-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="19421-109">參數</span><span class="sxs-lookup"><span data-stu-id="19421-109">Parameters</span></span>

<span data-ttu-id="19421-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="19421-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="19421-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="19421-111">Return value</span></span>

<span data-ttu-id="19421-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19421-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19421-113">備註</span><span class="sxs-lookup"><span data-stu-id="19421-113">Remarks</span></span>

<span data-ttu-id="19421-114">在容器處理的全螢幕模式中，容器應進入標準全螢幕模式，以回應此事件。</span><span class="sxs-lookup"><span data-stu-id="19421-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="19421-115">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="19421-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19421-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="19421-116">Requirements</span></span>



| <span data-ttu-id="19421-117">需求</span><span class="sxs-lookup"><span data-stu-id="19421-117">Requirement</span></span> | <span data-ttu-id="19421-118">值</span><span class="sxs-lookup"><span data-stu-id="19421-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19421-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19421-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19421-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19421-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19421-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19421-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19421-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19421-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19421-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="19421-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="19421-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19421-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="19421-125">DLL</span><span class="sxs-lookup"><span data-stu-id="19421-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19421-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19421-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="19421-127">IID</span><span class="sxs-lookup"><span data-stu-id="19421-127">IID</span></span><br/>                      | <span data-ttu-id="19421-128">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="19421-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="19421-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19421-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19421-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="19421-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





