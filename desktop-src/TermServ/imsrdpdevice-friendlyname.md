---
title: IMsRdpDevice FriendlyName 屬性
description: 抓取裝置的顯示名稱。
ms.assetid: ed27eacd-1d39-484c-8217-62ed608db050
ms.tgt_platform: multiple
keywords:
- FriendlyName 屬性遠端桌面服務
- FriendlyName 屬性遠端桌面服務，IMsRdpDevice 介面
- IMsRdpDevice 介面遠端桌面服務，FriendlyName 屬性
topic_type:
- apiref
api_name:
- IMsRdpDevice.FriendlyName
- IMsRdpDevice.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf7963cf49945b886d72a622b517438e24d148f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685668"
---
# <a name="imsrdpdevicefriendlyname-property"></a><span data-ttu-id="85dd6-106">IMsRdpDevice：： FriendlyName 屬性</span><span class="sxs-lookup"><span data-stu-id="85dd6-106">IMsRdpDevice::FriendlyName property</span></span>

<span data-ttu-id="85dd6-107">抓取裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="85dd6-107">Retrieves the display name for the device.</span></span>

<span data-ttu-id="85dd6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="85dd6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dd6-109">語法</span><span class="sxs-lookup"><span data-stu-id="85dd6-109">Syntax</span></span>


```C++
HRESULT get_FriendlyName(
  [out] BSTR *pFriendlyName
);
```



## <a name="property-value"></a><span data-ttu-id="85dd6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="85dd6-110">Property value</span></span>

<span data-ttu-id="85dd6-111">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="85dd6-111">The display name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85dd6-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="85dd6-112">Error codes</span></span>

<span data-ttu-id="85dd6-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="85dd6-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="85dd6-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="85dd6-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="85dd6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="85dd6-115">Requirements</span></span>



| <span data-ttu-id="85dd6-116">需求</span><span class="sxs-lookup"><span data-stu-id="85dd6-116">Requirement</span></span> | <span data-ttu-id="85dd6-117">值</span><span class="sxs-lookup"><span data-stu-id="85dd6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85dd6-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="85dd6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85dd6-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85dd6-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85dd6-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="85dd6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85dd6-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85dd6-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85dd6-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="85dd6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="85dd6-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85dd6-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="85dd6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="85dd6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85dd6-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85dd6-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="85dd6-126">IID</span><span class="sxs-lookup"><span data-stu-id="85dd6-126">IID</span></span><br/>                      | <span data-ttu-id="85dd6-127">IID \_ IMsRdpDevice 定義為60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="85dd6-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="85dd6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85dd6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dd6-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="85dd6-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





