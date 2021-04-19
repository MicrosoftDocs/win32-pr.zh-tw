---
title: IMsRdpDeviceCollection RescanDevices 方法
description: 重新整理集合中的物件清單。 |IMsRdpDeviceCollection RescanDevices 方法
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- RescanDevices 方法遠端桌面服務
- RescanDevices 方法遠端桌面服務，IMsRdpDeviceCollection 介面
- IMsRdpDeviceCollection 介面遠端桌面服務，RescanDevices 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988147"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="adf5b-107">IMsRdpDeviceCollection：： RescanDevices 方法</span><span class="sxs-lookup"><span data-stu-id="adf5b-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="adf5b-108">重新整理集合中的物件清單。</span><span class="sxs-lookup"><span data-stu-id="adf5b-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf5b-109">語法</span><span class="sxs-lookup"><span data-stu-id="adf5b-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="adf5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="adf5b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf5b-111">*vboolDynRedir* \[在\]</span><span class="sxs-lookup"><span data-stu-id="adf5b-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf5b-112">預設會套用至任何新探索到的裝置或磁片磁碟機的重新導向狀態。</span><span class="sxs-lookup"><span data-stu-id="adf5b-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf5b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="adf5b-113">Return value</span></span>

<span data-ttu-id="adf5b-114">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="adf5b-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="adf5b-115">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="adf5b-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf5b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="adf5b-116">Requirements</span></span>



| <span data-ttu-id="adf5b-117">需求</span><span class="sxs-lookup"><span data-stu-id="adf5b-117">Requirement</span></span> | <span data-ttu-id="adf5b-118">值</span><span class="sxs-lookup"><span data-stu-id="adf5b-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf5b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adf5b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="adf5b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adf5b-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="adf5b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adf5b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="adf5b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adf5b-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="adf5b-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="adf5b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="adf5b-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf5b-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="adf5b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="adf5b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf5b-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf5b-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="adf5b-127">IID</span><span class="sxs-lookup"><span data-stu-id="adf5b-127">IID</span></span><br/>                      | <span data-ttu-id="adf5b-128">IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="adf5b-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="adf5b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adf5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf5b-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="adf5b-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





