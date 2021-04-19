---
title: IMsTscAxEvents OnUserNameAcquired 方法
description: 當控制項取得使用者名稱時呼叫。
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- OnUserNameAcquired 方法遠端桌面服務
- OnUserNameAcquired 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnUserNameAcquired 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965914"
---
# <a name="imstscaxeventsonusernameacquired-method"></a><span data-ttu-id="daf4d-106">IMsTscAxEvents：： OnUserNameAcquired 方法</span><span class="sxs-lookup"><span data-stu-id="daf4d-106">IMsTscAxEvents::OnUserNameAcquired method</span></span>

<span data-ttu-id="daf4d-107">當控制項取得使用者名稱時呼叫。</span><span class="sxs-lookup"><span data-stu-id="daf4d-107">Called when the user name has been acquired by the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf4d-108">語法</span><span class="sxs-lookup"><span data-stu-id="daf4d-108">Syntax</span></span>


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a><span data-ttu-id="daf4d-109">參數</span><span class="sxs-lookup"><span data-stu-id="daf4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf4d-110">*bstrUserName*</span><span class="sxs-lookup"><span data-stu-id="daf4d-110">*bstrUserName*</span></span> 
</dt> <dd>

<span data-ttu-id="daf4d-111">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="daf4d-111">The user name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf4d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="daf4d-112">Return value</span></span>

<span data-ttu-id="daf4d-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="daf4d-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf4d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="daf4d-114">Requirements</span></span>



| <span data-ttu-id="daf4d-115">需求</span><span class="sxs-lookup"><span data-stu-id="daf4d-115">Requirement</span></span> | <span data-ttu-id="daf4d-116">值</span><span class="sxs-lookup"><span data-stu-id="daf4d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="daf4d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="daf4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="daf4d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="daf4d-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="daf4d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="daf4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="daf4d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="daf4d-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="daf4d-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="daf4d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="daf4d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf4d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="daf4d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="daf4d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf4d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf4d-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="daf4d-125">IID</span><span class="sxs-lookup"><span data-stu-id="daf4d-125">IID</span></span><br/>                      | <span data-ttu-id="daf4d-126">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="daf4d-126">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="daf4d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="daf4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf4d-128">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="daf4d-128">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





