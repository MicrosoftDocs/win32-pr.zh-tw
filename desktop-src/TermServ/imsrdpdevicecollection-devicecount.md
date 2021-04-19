---
title: IMsRdpDeviceCollection DeviceCount 屬性
description: 抓取集合中的物件計數。 |IMsRdpDeviceCollection DeviceCount 屬性
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- DeviceCount 屬性遠端桌面服務
- DeviceCount 屬性遠端桌面服務，IMsRdpDeviceCollection 介面
- IMsRdpDeviceCollection 介面遠端桌面服務，DeviceCount 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106984270"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="c68d7-107">IMsRdpDeviceCollection：:D eviceCount 屬性</span><span class="sxs-lookup"><span data-stu-id="c68d7-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="c68d7-108">抓取集合中的物件計數。</span><span class="sxs-lookup"><span data-stu-id="c68d7-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="c68d7-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c68d7-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68d7-110">語法</span><span class="sxs-lookup"><span data-stu-id="c68d7-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="c68d7-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="c68d7-111">Property value</span></span>

<span data-ttu-id="c68d7-112">物件計數。</span><span class="sxs-lookup"><span data-stu-id="c68d7-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c68d7-113">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c68d7-113">Error codes</span></span>

<span data-ttu-id="c68d7-114">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c68d7-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c68d7-115">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="c68d7-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68d7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c68d7-116">Requirements</span></span>



| <span data-ttu-id="c68d7-117">需求</span><span class="sxs-lookup"><span data-stu-id="c68d7-117">Requirement</span></span> | <span data-ttu-id="c68d7-118">值</span><span class="sxs-lookup"><span data-stu-id="c68d7-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68d7-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c68d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c68d7-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c68d7-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c68d7-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c68d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c68d7-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c68d7-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c68d7-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c68d7-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c68d7-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68d7-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c68d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c68d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c68d7-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c68d7-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c68d7-127">IID</span><span class="sxs-lookup"><span data-stu-id="c68d7-127">IID</span></span><br/>                      | <span data-ttu-id="c68d7-128">IID \_ IMsRdpDeviceCollection 定義為 56540617-d281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="c68d7-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c68d7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c68d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68d7-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="c68d7-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





