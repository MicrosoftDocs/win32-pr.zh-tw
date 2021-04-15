---
title: IMsRdpDeviceCollection DeviceByIndex 屬性
description: 在指定的索引處抓取裝置。
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- DeviceByIndex 屬性遠端桌面服務
- DeviceByIndex 屬性遠端桌面服務，IMsRdpDeviceCollection 介面
- IMsRdpDeviceCollection 介面遠端桌面服務，DeviceByIndex 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467017"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="0356c-106">IMsRdpDeviceCollection：:D eviceByIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="0356c-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="0356c-107">在指定的索引處抓取裝置。</span><span class="sxs-lookup"><span data-stu-id="0356c-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="0356c-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0356c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0356c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0356c-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="0356c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0356c-110">Property value</span></span>

<span data-ttu-id="0356c-111">[**IMsRdpDevice**](imsrdpdevice.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="0356c-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0356c-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0356c-112">Error codes</span></span>

<span data-ttu-id="0356c-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0356c-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="0356c-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="0356c-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0356c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0356c-115">Requirements</span></span>



| <span data-ttu-id="0356c-116">需求</span><span class="sxs-lookup"><span data-stu-id="0356c-116">Requirement</span></span> | <span data-ttu-id="0356c-117">值</span><span class="sxs-lookup"><span data-stu-id="0356c-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0356c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0356c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0356c-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0356c-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="0356c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0356c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0356c-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0356c-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0356c-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0356c-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="0356c-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0356c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0356c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0356c-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0356c-126">IID</span><span class="sxs-lookup"><span data-stu-id="0356c-126">IID</span></span><br/>                      | <span data-ttu-id="0356c-127">IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="0356c-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0356c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0356c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0356c-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="0356c-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





