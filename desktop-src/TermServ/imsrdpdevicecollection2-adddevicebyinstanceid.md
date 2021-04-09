---
title: IMsRdpDeviceCollection2 AddDeviceByInstanceId 方法
description: 將未列出的裝置新增至裝置集合。
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- AddDeviceByInstanceId 方法遠端桌面服務
- AddDeviceByInstanceId 方法遠端桌面服務，IMsRdpDeviceCollection2 介面
- IMsRdpDeviceCollection2 介面遠端桌面服務，AddDeviceByInstanceId 方法
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024612"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="99b6d-106">IMsRdpDeviceCollection2：： AddDeviceByInstanceId 方法</span><span class="sxs-lookup"><span data-stu-id="99b6d-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="99b6d-107">將未列出的裝置新增至裝置集合。</span><span class="sxs-lookup"><span data-stu-id="99b6d-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b6d-108">語法</span><span class="sxs-lookup"><span data-stu-id="99b6d-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="99b6d-109">參數</span><span class="sxs-lookup"><span data-stu-id="99b6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b6d-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b6d-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b6d-111">類型： **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="99b6d-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="99b6d-112">[**RedirectDeviceType**](redirectdevicetype.md)列舉的值，這個值會指定要新增的裝置類型。</span><span class="sxs-lookup"><span data-stu-id="99b6d-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="99b6d-113">*InstanceId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b6d-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b6d-114">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="99b6d-114">Type: **BSTR**</span></span>

<span data-ttu-id="99b6d-115">要加入之裝置的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="99b6d-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b6d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="99b6d-116">Return value</span></span>

<span data-ttu-id="99b6d-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="99b6d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="99b6d-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="99b6d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99b6d-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99b6d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b6d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="99b6d-120">Requirements</span></span>



| <span data-ttu-id="99b6d-121">需求</span><span class="sxs-lookup"><span data-stu-id="99b6d-121">Requirement</span></span> | <span data-ttu-id="99b6d-122">值</span><span class="sxs-lookup"><span data-stu-id="99b6d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b6d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99b6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99b6d-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="99b6d-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="99b6d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99b6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99b6d-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99b6d-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="99b6d-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="99b6d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="99b6d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b6d-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="99b6d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="99b6d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b6d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b6d-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b6d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99b6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b6d-132">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="99b6d-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="99b6d-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="99b6d-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





