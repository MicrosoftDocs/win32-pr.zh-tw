---
title: 'IVMSerialPortCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的序列埠數目。
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMSerialPortCollection 介面
- IVMSerialPortCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbf0503f00fd1df7d27a8eeafedd3efe42619b98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843835"
---
# <a name="ivmserialportcollectioncount-property"></a><span data-ttu-id="67fe9-106">IVMSerialPortCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="67fe9-106">IVMSerialPortCollection::Count property</span></span>

<span data-ttu-id="67fe9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="67fe9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="67fe9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="67fe9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="67fe9-109">抓取此集合中的序列埠數目。</span><span class="sxs-lookup"><span data-stu-id="67fe9-109">Retrieves the number of serial ports in this collection.</span></span>

<span data-ttu-id="67fe9-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="67fe9-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fe9-111">語法</span><span class="sxs-lookup"><span data-stu-id="67fe9-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="67fe9-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="67fe9-112">Property value</span></span>

<span data-ttu-id="67fe9-113">序列埠的數目。</span><span class="sxs-lookup"><span data-stu-id="67fe9-113">The number of serial ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="67fe9-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="67fe9-114">Error codes</span></span>



| <span data-ttu-id="67fe9-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="67fe9-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="67fe9-116">意義</span><span class="sxs-lookup"><span data-stu-id="67fe9-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="67fe9-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67fe9-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="67fe9-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="67fe9-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="67fe9-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="67fe9-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="67fe9-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="67fe9-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="67fe9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="67fe9-121">Requirements</span></span>



| <span data-ttu-id="67fe9-122">需求</span><span class="sxs-lookup"><span data-stu-id="67fe9-122">Requirement</span></span> | <span data-ttu-id="67fe9-123">值</span><span class="sxs-lookup"><span data-stu-id="67fe9-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fe9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67fe9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="67fe9-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67fe9-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67fe9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67fe9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="67fe9-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="67fe9-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="67fe9-128">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="67fe9-128">End of client support</span></span><br/>    | <span data-ttu-id="67fe9-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67fe9-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="67fe9-130">產品</span><span class="sxs-lookup"><span data-stu-id="67fe9-130">Product</span></span><br/>                  | <span data-ttu-id="67fe9-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="67fe9-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="67fe9-132">標頭</span><span class="sxs-lookup"><span data-stu-id="67fe9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="67fe9-133"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="67fe9-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="67fe9-134">IID</span><span class="sxs-lookup"><span data-stu-id="67fe9-134">IID</span></span><br/>                      | <span data-ttu-id="67fe9-135">IID \_ IVMSerialPortCollection 定義為 dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="67fe9-135">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="67fe9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67fe9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fe9-137">**IVMSerialPortCollection**</span><span class="sxs-lookup"><span data-stu-id="67fe9-137">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

