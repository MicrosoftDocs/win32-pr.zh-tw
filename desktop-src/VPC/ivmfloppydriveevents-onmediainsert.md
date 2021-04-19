---
title: 'IVMFloppyDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
description: '接收媒體已插入磁片磁碟機的通知。 |IVMFloppyDriveEvents OnMediaInsert 方法 (VPCCOMInterfaces .h) '
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- OnMediaInsert 方法 Virtual PC
- OnMediaInsert 方法 Virtual PC，IVMFloppyDriveEvents 介面
- IVMFloppyDriveEvents 介面 Virtual PC，OnMediaInsert 方法
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997235"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a><span data-ttu-id="3bd2f-107">IVMFloppyDriveEvents：： OnMediaInsert 方法</span><span class="sxs-lookup"><span data-stu-id="3bd2f-107">IVMFloppyDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="3bd2f-108">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3bd2f-109">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3bd2f-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3bd2f-110">接收媒體已插入磁片磁碟機的通知。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd2f-111">語法</span><span class="sxs-lookup"><span data-stu-id="3bd2f-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="3bd2f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3bd2f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd2f-113">*mediaPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd2f-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd2f-114">磁片磁碟機的主機磁碟機號或路徑。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-114">The host drive letter, or path, to floppy image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd2f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bd2f-115">Return value</span></span>

<span data-ttu-id="3bd2f-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3bd2f-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd2f-118">備註</span><span class="sxs-lookup"><span data-stu-id="3bd2f-118">Remarks</span></span>

<span data-ttu-id="3bd2f-119">當媒體 (磁片影像，或插入主機磁片磁碟機) 中的磁片時，會呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-119">This method is called when media (a floppy disk image or a floppy disk in a host drive) is inserted.</span></span> <span data-ttu-id="3bd2f-120">用戶端程式必須執行這個介面方法，以接收來自 IVMFloppyDrive 的 vmFloppyDriveEvent \_ OnMediaInsert 事件的[](ivmfloppydrive.md)通知。</span><span class="sxs-lookup"><span data-stu-id="3bd2f-120">The client program must implement this interface method to receive notification of the vmFloppyDriveEvent\_OnMediaInsert event originating from [**IVMFloppyDrive**](ivmfloppydrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd2f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bd2f-121">Requirements</span></span>



| <span data-ttu-id="3bd2f-122">需求</span><span class="sxs-lookup"><span data-stu-id="3bd2f-122">Requirement</span></span> | <span data-ttu-id="3bd2f-123">值</span><span class="sxs-lookup"><span data-stu-id="3bd2f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd2f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bd2f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd2f-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3bd2f-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bd2f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bd2f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd2f-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="3bd2f-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3bd2f-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3bd2f-128">End of client support</span></span><br/>    | <span data-ttu-id="3bd2f-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3bd2f-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3bd2f-130">產品</span><span class="sxs-lookup"><span data-stu-id="3bd2f-130">Product</span></span><br/>                  | <span data-ttu-id="3bd2f-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3bd2f-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3bd2f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3bd2f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bd2f-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd2f-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd2f-134">IID</span><span class="sxs-lookup"><span data-stu-id="3bd2f-134">IID</span></span><br/>                      | <span data-ttu-id="3bd2f-135">DIID \_ IVMFloppyDriveEvents 定義為 a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="3bd2f-135">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3bd2f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bd2f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd2f-137">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="3bd2f-137">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

