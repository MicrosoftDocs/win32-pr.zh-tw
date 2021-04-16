---
title: IMsTscAxEvents OnDevicesButtonPressed 方法
description: 當按下連接列中的 [裝置] 按鈕時呼叫。
ms.assetid: E2B1780F-EDD9-4C11-A887-10586145240E
ms.tgt_platform: multiple
keywords:
- OnDevicesButtonPressed 方法遠端桌面服務
- OnDevicesButtonPressed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnDevicesButtonPressed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDevicesButtonPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7846dfefa7d093e52cad58fa13335a6b633c82b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508376"
---
# <a name="imstscaxeventsondevicesbuttonpressed-method"></a><span data-ttu-id="13a33-106">IMsTscAxEvents：： OnDevicesButtonPressed 方法</span><span class="sxs-lookup"><span data-stu-id="13a33-106">IMsTscAxEvents::OnDevicesButtonPressed method</span></span>

<span data-ttu-id="13a33-107">當按下連接列中的 [裝置] 按鈕時呼叫。</span><span class="sxs-lookup"><span data-stu-id="13a33-107">Called when the devices button in the connection bar has been pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a33-108">語法</span><span class="sxs-lookup"><span data-stu-id="13a33-108">Syntax</span></span>


```C++
void OnDevicesButtonPressed();
```



## <a name="parameters"></a><span data-ttu-id="13a33-109">參數</span><span class="sxs-lookup"><span data-stu-id="13a33-109">Parameters</span></span>

<span data-ttu-id="13a33-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="13a33-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13a33-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a33-111">Return value</span></span>

<span data-ttu-id="13a33-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="13a33-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a33-113">備註</span><span class="sxs-lookup"><span data-stu-id="13a33-113">Remarks</span></span>

<span data-ttu-id="13a33-114">當用戶端和伺服器上同時啟用 USB 重新導向時，[裝置] 按鈕會顯示在連接列中。</span><span class="sxs-lookup"><span data-stu-id="13a33-114">The devices button is displayed in the connection bar when USB redirection is enabled on both the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a33-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a33-115">Requirements</span></span>



| <span data-ttu-id="13a33-116">需求</span><span class="sxs-lookup"><span data-stu-id="13a33-116">Requirement</span></span> | <span data-ttu-id="13a33-117">值</span><span class="sxs-lookup"><span data-stu-id="13a33-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13a33-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13a33-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13a33-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="13a33-119">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="13a33-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13a33-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13a33-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13a33-121">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="13a33-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="13a33-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="13a33-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a33-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="13a33-124">DLL</span><span class="sxs-lookup"><span data-stu-id="13a33-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a33-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a33-125"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a33-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13a33-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a33-127">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="13a33-127">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





