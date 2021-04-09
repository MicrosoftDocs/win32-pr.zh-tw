---
title: 'IVMDVDDriveEvents OnMediaEject 方法 (VPCCOMInterfaces .h) '
description: '接收媒體已從磁片磁碟機中取出的通知。 |IVMDVDDriveEvents OnMediaEject 方法 (VPCCOMInterfaces .h) '
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- OnMediaEject 方法 Virtual PC
- OnMediaEject 方法 Virtual PC，IVMDVDDriveEvents 介面
- IVMDVDDriveEvents 介面 Virtual PC，OnMediaEject 方法
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853619"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a><span data-ttu-id="7b13b-107">IVMDVDDriveEvents：： OnMediaEject 方法</span><span class="sxs-lookup"><span data-stu-id="7b13b-107">IVMDVDDriveEvents::OnMediaEject method</span></span>

<span data-ttu-id="7b13b-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7b13b-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7b13b-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7b13b-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7b13b-110">接收媒體已從磁片磁碟機中取出的通知。</span><span class="sxs-lookup"><span data-stu-id="7b13b-110">Receives notification that media has been ejected from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b13b-111">語法</span><span class="sxs-lookup"><span data-stu-id="7b13b-111">Syntax</span></span>


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="7b13b-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b13b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b13b-113">*mediaPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7b13b-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b13b-114">ISO 映像的主機磁碟機號或路徑。</span><span class="sxs-lookup"><span data-stu-id="7b13b-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b13b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b13b-115">Return value</span></span>

<span data-ttu-id="7b13b-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7b13b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b13b-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7b13b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b13b-118">備註</span><span class="sxs-lookup"><span data-stu-id="7b13b-118">Remarks</span></span>

<span data-ttu-id="7b13b-119">當媒體 (ISO 映像或主機磁片磁碟機中的光碟) 時，會呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="7b13b-119">This method is called when media (an ISO image or a disc in a host drive) is ejected.</span></span> <span data-ttu-id="7b13b-120">用戶端程式必須執行這個介面方法，以接收來自 IVMDVDDrive 的 vmDVDDriveEvent \_ OnEject 事件的[](ivmdvddrive.md)通知。</span><span class="sxs-lookup"><span data-stu-id="7b13b-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnEject event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b13b-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b13b-121">Requirements</span></span>



| <span data-ttu-id="7b13b-122">需求</span><span class="sxs-lookup"><span data-stu-id="7b13b-122">Requirement</span></span> | <span data-ttu-id="7b13b-123">值</span><span class="sxs-lookup"><span data-stu-id="7b13b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b13b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b13b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7b13b-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b13b-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b13b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b13b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7b13b-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="7b13b-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7b13b-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7b13b-128">End of client support</span></span><br/>    | <span data-ttu-id="7b13b-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b13b-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7b13b-130">產品</span><span class="sxs-lookup"><span data-stu-id="7b13b-130">Product</span></span><br/>                  | <span data-ttu-id="7b13b-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7b13b-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7b13b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7b13b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b13b-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b13b-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7b13b-134">IID</span><span class="sxs-lookup"><span data-stu-id="7b13b-134">IID</span></span><br/>                      | <span data-ttu-id="7b13b-135">DIID \_ IVMDVDDriveEvents 定義為 c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="7b13b-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7b13b-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b13b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b13b-137">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="7b13b-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

