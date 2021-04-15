---
title: IMsRdpDeviceCollection DeviceById 屬性
description: 使用指定的識別碼抓取裝置。
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- DeviceById 屬性遠端桌面服務
- DeviceById 屬性遠端桌面服務，IMsRdpDeviceCollection 介面
- IMsRdpDeviceCollection 介面遠端桌面服務，DeviceById 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465129"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="01433-106">IMsRdpDeviceCollection：:D eviceById 屬性</span><span class="sxs-lookup"><span data-stu-id="01433-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="01433-107">使用指定的識別碼抓取裝置。</span><span class="sxs-lookup"><span data-stu-id="01433-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="01433-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="01433-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01433-109">語法</span><span class="sxs-lookup"><span data-stu-id="01433-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="01433-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="01433-110">Property value</span></span>

<span data-ttu-id="01433-111">[**IMsRdpDevice**](imsrdpdevice.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="01433-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01433-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="01433-112">Error codes</span></span>

<span data-ttu-id="01433-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="01433-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="01433-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="01433-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="01433-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="01433-115">Requirements</span></span>



| <span data-ttu-id="01433-116">需求</span><span class="sxs-lookup"><span data-stu-id="01433-116">Requirement</span></span> | <span data-ttu-id="01433-117">值</span><span class="sxs-lookup"><span data-stu-id="01433-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="01433-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01433-118">Minimum supported client</span></span><br/> | <span data-ttu-id="01433-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01433-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="01433-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01433-120">Minimum supported server</span></span><br/> | <span data-ttu-id="01433-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01433-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="01433-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="01433-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="01433-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01433-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="01433-124">DLL</span><span class="sxs-lookup"><span data-stu-id="01433-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01433-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01433-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="01433-126">IID</span><span class="sxs-lookup"><span data-stu-id="01433-126">IID</span></span><br/>                      | <span data-ttu-id="01433-127">IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="01433-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01433-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01433-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01433-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="01433-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





