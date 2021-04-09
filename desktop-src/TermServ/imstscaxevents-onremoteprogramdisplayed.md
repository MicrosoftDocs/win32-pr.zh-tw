---
title: IMsTscAxEvents OnRemoteProgramDisplayed 方法
description: 在顯示 RemoteApp 程式時呼叫。
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- OnRemoteProgramDisplayed 方法遠端桌面服務
- OnRemoteProgramDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnRemoteProgramDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686060"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="79139-106">IMsTscAxEvents：： OnRemoteProgramDisplayed 方法</span><span class="sxs-lookup"><span data-stu-id="79139-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="79139-107">在顯示 RemoteApp 程式時呼叫。</span><span class="sxs-lookup"><span data-stu-id="79139-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="79139-108">語法</span><span class="sxs-lookup"><span data-stu-id="79139-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="79139-109">參數</span><span class="sxs-lookup"><span data-stu-id="79139-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79139-110">*vbDisplayed* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79139-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79139-111">指出是否要顯示或隱藏 RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="79139-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="79139-112">*uDisplayInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79139-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79139-113">顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="79139-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="79139-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**鐵路 \_ APPDISPLAY \_ AUTORECONNECT**</span><span class="sxs-lookup"><span data-stu-id="79139-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="79139-115">自動重新連線正在進行中。</span><span class="sxs-lookup"><span data-stu-id="79139-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="79139-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**鐵路 \_ APPDISPLAY \_ DESKTOPHOOKED**</span><span class="sxs-lookup"><span data-stu-id="79139-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="79139-117">RemoteApp 計數只會進入零。</span><span class="sxs-lookup"><span data-stu-id="79139-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79139-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="79139-118">Return value</span></span>

<span data-ttu-id="79139-119">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="79139-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79139-120">備註</span><span class="sxs-lookup"><span data-stu-id="79139-120">Remarks</span></span>

<span data-ttu-id="79139-121">在事件接收中執行此方法，以接收已顯示 RemoteApp 的通知。</span><span class="sxs-lookup"><span data-stu-id="79139-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="79139-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="79139-122">Requirements</span></span>



| <span data-ttu-id="79139-123">需求</span><span class="sxs-lookup"><span data-stu-id="79139-123">Requirement</span></span> | <span data-ttu-id="79139-124">值</span><span class="sxs-lookup"><span data-stu-id="79139-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79139-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79139-125">Minimum supported client</span></span><br/> | <span data-ttu-id="79139-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="79139-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="79139-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79139-127">Minimum supported server</span></span><br/> | <span data-ttu-id="79139-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79139-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="79139-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="79139-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="79139-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79139-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79139-131">DLL</span><span class="sxs-lookup"><span data-stu-id="79139-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79139-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79139-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="79139-133">IID</span><span class="sxs-lookup"><span data-stu-id="79139-133">IID</span></span><br/>                      | <span data-ttu-id="79139-134">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="79139-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





