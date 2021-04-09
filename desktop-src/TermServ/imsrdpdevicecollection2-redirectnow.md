---
title: IMsRdpDeviceCollection2 RedirectNow 方法
description: 強制將從集合中選取或取消選取的裝置重新導向或移除。
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- RedirectNow 方法遠端桌面服務
- RedirectNow 方法遠端桌面服務，IMsRdpDeviceCollection2 介面
- IMsRdpDeviceCollection2 介面遠端桌面服務，RedirectNow 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933929"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="fbbbb-106">IMsRdpDeviceCollection2：： RedirectNow 方法</span><span class="sxs-lookup"><span data-stu-id="fbbbb-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="fbbbb-107">強制將從集合中選取或取消選取的裝置重新導向或移除。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbbb-108">語法</span><span class="sxs-lookup"><span data-stu-id="fbbbb-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="fbbbb-109">參數</span><span class="sxs-lookup"><span data-stu-id="fbbbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbbbb-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbbbb-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbbbb-111">類型： **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="fbbbb-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="fbbbb-112">[**RedirectDeviceType**](redirectdevicetype.md)列舉的值，指定要重新導向的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbbbb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbbbb-113">Return value</span></span>

<span data-ttu-id="fbbbb-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fbbbb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fbbbb-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fbbbb-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbbbb-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbbbb-117">Requirements</span></span>



| <span data-ttu-id="fbbbb-118">需求</span><span class="sxs-lookup"><span data-stu-id="fbbbb-118">Requirement</span></span> | <span data-ttu-id="fbbbb-119">值</span><span class="sxs-lookup"><span data-stu-id="fbbbb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbbb-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbbbb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbbb-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fbbbb-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="fbbbb-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbbbb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbbb-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbbbb-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="fbbbb-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fbbbb-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbbbb-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbbb-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fbbbb-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fbbbb-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbbbb-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbbb-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbbbb-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbbbb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbbb-129">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="fbbbb-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="fbbbb-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="fbbbb-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





