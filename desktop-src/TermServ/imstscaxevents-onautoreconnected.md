---
title: IMsTscAxEvents OnAutoReconnected 方法
description: 當用戶端控制項自動重新連接到遠端會話時呼叫。 |IMsTscAxEvents OnAutoReconnected 方法
ms.assetid: 50307002-33F9-453C-A880-AF4111412854
ms.tgt_platform: multiple
keywords:
- OnAutoReconnected 方法遠端桌面服務
- OnAutoReconnected 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAutoReconnected 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29f0e9a498a727614bdfda621c214199918e2ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106975627"
---
# <a name="imstscaxeventsonautoreconnected-method"></a><span data-ttu-id="4bcfd-107">IMsTscAxEvents：： OnAutoReconnected 方法</span><span class="sxs-lookup"><span data-stu-id="4bcfd-107">IMsTscAxEvents::OnAutoReconnected method</span></span>

<span data-ttu-id="4bcfd-108">當用戶端控制項自動重新連接到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="4bcfd-108">Called when the client control has automatically reconnected to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcfd-109">語法</span><span class="sxs-lookup"><span data-stu-id="4bcfd-109">Syntax</span></span>


```C++
HRESULT OnAutoReconnected();
```



## <a name="parameters"></a><span data-ttu-id="4bcfd-110">參數</span><span class="sxs-lookup"><span data-stu-id="4bcfd-110">Parameters</span></span>

<span data-ttu-id="4bcfd-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4bcfd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bcfd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bcfd-112">Return value</span></span>

<span data-ttu-id="4bcfd-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4bcfd-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bcfd-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4bcfd-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bcfd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bcfd-115">Requirements</span></span>



| <span data-ttu-id="4bcfd-116">需求</span><span class="sxs-lookup"><span data-stu-id="4bcfd-116">Requirement</span></span> | <span data-ttu-id="4bcfd-117">值</span><span class="sxs-lookup"><span data-stu-id="4bcfd-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcfd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bcfd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcfd-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4bcfd-119">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="4bcfd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bcfd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcfd-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bcfd-121">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="4bcfd-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="4bcfd-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bcfd-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcfd-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4bcfd-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcfd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcfd-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcfd-125"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bcfd-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bcfd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bcfd-127">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="4bcfd-127">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





