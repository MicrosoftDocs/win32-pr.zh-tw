---
title: IMsRdpDevice RedirectionState 屬性
description: 指出裝置的重新導向狀態。
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- RedirectionState 屬性遠端桌面服務
- RedirectionState 屬性遠端桌面服務，IMsRdpDevice 介面
- IMsRdpDevice 介面遠端桌面服務，RedirectionState 屬性
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465132"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="b1d59-106">IMsRdpDevice：： RedirectionState 屬性</span><span class="sxs-lookup"><span data-stu-id="b1d59-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="b1d59-107">指出裝置的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="b1d59-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="b1d59-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="b1d59-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d59-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1d59-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="b1d59-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="b1d59-110">Property value</span></span>

<span data-ttu-id="b1d59-111">將此參數設定為 **VARIANT \_ FALSE** ，以停用重新導向或 **variant \_ TRUE** 來啟用重新導向。</span><span class="sxs-lookup"><span data-stu-id="b1d59-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1d59-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b1d59-112">Error codes</span></span>

<span data-ttu-id="b1d59-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="b1d59-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="b1d59-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="b1d59-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d59-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1d59-115">Requirements</span></span>



| <span data-ttu-id="b1d59-116">需求</span><span class="sxs-lookup"><span data-stu-id="b1d59-116">Requirement</span></span> | <span data-ttu-id="b1d59-117">值</span><span class="sxs-lookup"><span data-stu-id="b1d59-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d59-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1d59-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d59-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1d59-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b1d59-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1d59-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d59-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1d59-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b1d59-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b1d59-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1d59-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1d59-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1d59-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b1d59-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1d59-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1d59-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1d59-126">IID</span><span class="sxs-lookup"><span data-stu-id="b1d59-126">IID</span></span><br/>                      | <span data-ttu-id="b1d59-127">IID \_ IMsRdpDevice 定義為60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="b1d59-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b1d59-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1d59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d59-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="b1d59-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





