---
title: IMsRdpDevice DeviceDescription 屬性
description: 抓取顯示名稱無法使用時，要向使用者顯示的裝置描述。
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- DeviceDescription 屬性遠端桌面服務
- DeviceDescription 屬性遠端桌面服務，IMsRdpDevice 介面
- IMsRdpDevice 介面遠端桌面服務，DeviceDescription 屬性
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104615"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="68e1a-106">IMsRdpDevice：:D eviceDescription 屬性</span><span class="sxs-lookup"><span data-stu-id="68e1a-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="68e1a-107">抓取顯示名稱無法使用時，要向使用者顯示的裝置描述。</span><span class="sxs-lookup"><span data-stu-id="68e1a-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="68e1a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="68e1a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68e1a-109">語法</span><span class="sxs-lookup"><span data-stu-id="68e1a-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="68e1a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="68e1a-110">Property value</span></span>

<span data-ttu-id="68e1a-111">裝置描述。</span><span class="sxs-lookup"><span data-stu-id="68e1a-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68e1a-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="68e1a-112">Error codes</span></span>

<span data-ttu-id="68e1a-113">如果方法成功，則會傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="68e1a-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="68e1a-114">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="68e1a-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="68e1a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="68e1a-115">Requirements</span></span>



| <span data-ttu-id="68e1a-116">需求</span><span class="sxs-lookup"><span data-stu-id="68e1a-116">Requirement</span></span> | <span data-ttu-id="68e1a-117">值</span><span class="sxs-lookup"><span data-stu-id="68e1a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68e1a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68e1a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="68e1a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68e1a-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68e1a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68e1a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="68e1a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68e1a-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68e1a-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68e1a-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="68e1a-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e1a-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68e1a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68e1a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68e1a-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68e1a-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68e1a-126">IID</span><span class="sxs-lookup"><span data-stu-id="68e1a-126">IID</span></span><br/>                      | <span data-ttu-id="68e1a-127">IID \_ IMsRdpDevice 定義為60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="68e1a-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="68e1a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68e1a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68e1a-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="68e1a-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





