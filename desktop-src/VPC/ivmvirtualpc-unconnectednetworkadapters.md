---
title: 'IVMVirtualPC UnconnectedNetworkAdapters 屬性 (VPCCOMInterfaces .h) '
description: 抓取未連接網路介面的可列舉集合。
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- UnconnectedNetworkAdapters 屬性 Virtual PC
- UnconnectedNetworkAdapters 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，UnconnectedNetworkAdapters 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025222"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a><span data-ttu-id="1a473-106">IVMVirtualPC：： UnconnectedNetworkAdapters 屬性</span><span class="sxs-lookup"><span data-stu-id="1a473-106">IVMVirtualPC::UnconnectedNetworkAdapters property</span></span>

<span data-ttu-id="1a473-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="1a473-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1a473-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="1a473-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1a473-109">抓取未連接網路介面的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="1a473-109">Retrieves an enumerable collection of unconnected network interfaces.</span></span>

<span data-ttu-id="1a473-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1a473-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a473-111">語法</span><span class="sxs-lookup"><span data-stu-id="1a473-111">Syntax</span></span>


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="1a473-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="1a473-112">Property value</span></span>

<span data-ttu-id="1a473-113">未連接的 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件集合。</span><span class="sxs-lookup"><span data-stu-id="1a473-113">A collection of unconnected [**IVMNetworkAdapter**](ivmnetworkadapter.md) objects.</span></span> <span data-ttu-id="1a473-114">請參閱 [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)。</span><span class="sxs-lookup"><span data-stu-id="1a473-114">See [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a473-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1a473-115">Error codes</span></span>



| <span data-ttu-id="1a473-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="1a473-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="1a473-117">意義</span><span class="sxs-lookup"><span data-stu-id="1a473-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a473-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1a473-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="1a473-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1a473-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1a473-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1a473-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="1a473-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1a473-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="1a473-122"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1a473-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="1a473-123">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a473-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="1a473-124"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="1a473-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="1a473-125">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="1a473-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1a473-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a473-126">Requirements</span></span>



| <span data-ttu-id="1a473-127">需求</span><span class="sxs-lookup"><span data-stu-id="1a473-127">Requirement</span></span> | <span data-ttu-id="1a473-128">值</span><span class="sxs-lookup"><span data-stu-id="1a473-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a473-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a473-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a473-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a473-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a473-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a473-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a473-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="1a473-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1a473-133">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1a473-133">End of client support</span></span><br/>    | <span data-ttu-id="1a473-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1a473-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1a473-135">產品</span><span class="sxs-lookup"><span data-stu-id="1a473-135">Product</span></span><br/>                  | <span data-ttu-id="1a473-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1a473-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1a473-137">標頭</span><span class="sxs-lookup"><span data-stu-id="1a473-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a473-138"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a473-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1a473-139">IID</span><span class="sxs-lookup"><span data-stu-id="1a473-139">IID</span></span><br/>                      | <span data-ttu-id="1a473-140">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="1a473-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1a473-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a473-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a473-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="1a473-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

