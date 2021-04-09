---
title: IMsRdpClientNonScriptable5 GetRemoteMonitorsBoundingBox 屬性
description: 指定遠端監視的周框。
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- GetRemoteMonitorsBoundingBox 屬性遠端桌面服務
- GetRemoteMonitorsBoundingBox 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，GetRemoteMonitorsBoundingBox 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934665"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="e8b31-106">IMsRdpClientNonScriptable5：： GetRemoteMonitorsBoundingBox 屬性</span><span class="sxs-lookup"><span data-stu-id="e8b31-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="e8b31-107">指定遠端監視的周框。</span><span class="sxs-lookup"><span data-stu-id="e8b31-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="e8b31-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e8b31-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b31-109">語法</span><span class="sxs-lookup"><span data-stu-id="e8b31-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="e8b31-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8b31-110">Property value</span></span>

<span data-ttu-id="e8b31-111">接收矩形的左邊緣。</span><span class="sxs-lookup"><span data-stu-id="e8b31-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="e8b31-112">接收矩形的上邊緣。</span><span class="sxs-lookup"><span data-stu-id="e8b31-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="e8b31-113">接收矩形的右邊緣。</span><span class="sxs-lookup"><span data-stu-id="e8b31-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="e8b31-114">接收矩形的下邊緣。</span><span class="sxs-lookup"><span data-stu-id="e8b31-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b31-115">備註</span><span class="sxs-lookup"><span data-stu-id="e8b31-115">Remarks</span></span>

<span data-ttu-id="e8b31-116">所有座標都是虛擬螢幕座標，相對於主要監視器的左上角。</span><span class="sxs-lookup"><span data-stu-id="e8b31-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="e8b31-117">如果這不是主要監視器，則部分或全部的值可能是負數。</span><span class="sxs-lookup"><span data-stu-id="e8b31-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b31-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8b31-118">Requirements</span></span>



| <span data-ttu-id="e8b31-119">需求</span><span class="sxs-lookup"><span data-stu-id="e8b31-119">Requirement</span></span> | <span data-ttu-id="e8b31-120">值</span><span class="sxs-lookup"><span data-stu-id="e8b31-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b31-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8b31-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b31-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8b31-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e8b31-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8b31-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b31-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e8b31-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e8b31-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e8b31-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8b31-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8b31-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8b31-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e8b31-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8b31-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8b31-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8b31-129">IID</span><span class="sxs-lookup"><span data-stu-id="e8b31-129">IID</span></span><br/>                      | <span data-ttu-id="e8b31-130">IID \_ IMsRdpClientNonScriptable5 定義為 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="e8b31-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8b31-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8b31-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b31-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e8b31-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





