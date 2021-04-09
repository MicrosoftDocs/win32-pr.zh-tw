---
title: 'IVMVirtualNetwork HostAdapter 屬性 (VPCCOMInterfaces .h) '
description: 虛擬網路連線的介面卡名稱。
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- HostAdapter 屬性 Virtual PC
- HostAdapter 屬性 Virtual PC，IVMVirtualNetwork 介面
- IVMVirtualNetwork 介面 Virtual PC，HostAdapter 屬性
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025353"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="00dba-106">IVMVirtualNetwork：： HostAdapter 屬性</span><span class="sxs-lookup"><span data-stu-id="00dba-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="00dba-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="00dba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00dba-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="00dba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00dba-109">抓取虛擬網路所連接的介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="00dba-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="00dba-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="00dba-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00dba-111">語法</span><span class="sxs-lookup"><span data-stu-id="00dba-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="00dba-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="00dba-112">Property value</span></span>

<span data-ttu-id="00dba-113">虛擬網路所連接之主機介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="00dba-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00dba-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="00dba-114">Error codes</span></span>



| <span data-ttu-id="00dba-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="00dba-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="00dba-116">意義</span><span class="sxs-lookup"><span data-stu-id="00dba-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00dba-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00dba-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="00dba-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="00dba-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="00dba-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="00dba-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="00dba-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="00dba-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="00dba-121"><dt>VM \_\_ \_ \_ 找不到電子 ADAPTER</dt> <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="00dba-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="00dba-122">此虛擬網路連線的主機乙太網路介面卡已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="00dba-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="00dba-123">主機乙太網路介面卡可能已移除或停用。</span><span class="sxs-lookup"><span data-stu-id="00dba-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="00dba-124"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="00dba-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="00dba-125">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="00dba-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="00dba-126">備註</span><span class="sxs-lookup"><span data-stu-id="00dba-126">Remarks</span></span>

<span data-ttu-id="00dba-127">虛擬網路介面卡可讓虛擬網路與外部網路通訊。</span><span class="sxs-lookup"><span data-stu-id="00dba-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="00dba-128">在主機電腦上安裝的每個乙太網路介面卡通常都有一個介面卡。</span><span class="sxs-lookup"><span data-stu-id="00dba-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="00dba-129">例如，假設主機電腦有一個標示為 "10/100 ENET" 的介面卡。</span><span class="sxs-lookup"><span data-stu-id="00dba-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="00dba-130">若要將虛擬 NIC 連線到連接至 "10/100 ENET" 的網路，請將虛擬網路的 Network **HostAdapter** 屬性設定為 "10/100 ENET"，並將虛擬 nic 連線到此虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="00dba-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="00dba-131">如果 **HostAdapter** 屬性設定為空字串 ( "" ) ，虛擬 NIC 介面卡會連線到「內部網路」或「共用網路 (NAT) 」網路。</span><span class="sxs-lookup"><span data-stu-id="00dba-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="00dba-132">連接至「內部網路」網路的虛擬 Nic 將無法存取系統主機上的外部網路。</span><span class="sxs-lookup"><span data-stu-id="00dba-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="00dba-133">不過，連接到此虛擬網路的虛擬 Nic 仍可彼此通訊。</span><span class="sxs-lookup"><span data-stu-id="00dba-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="00dba-134">您可以透過 [**IVMHostInfo：： NetworkAdapters**](ivmhostinfo-networkadapters.md) 屬性來存取完整的介面卡清單。</span><span class="sxs-lookup"><span data-stu-id="00dba-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="00dba-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="00dba-135">Requirements</span></span>



| <span data-ttu-id="00dba-136">需求</span><span class="sxs-lookup"><span data-stu-id="00dba-136">Requirement</span></span> | <span data-ttu-id="00dba-137">值</span><span class="sxs-lookup"><span data-stu-id="00dba-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00dba-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00dba-138">Minimum supported client</span></span><br/> | <span data-ttu-id="00dba-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00dba-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00dba-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00dba-140">Minimum supported server</span></span><br/> | <span data-ttu-id="00dba-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="00dba-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00dba-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="00dba-142">End of client support</span></span><br/>    | <span data-ttu-id="00dba-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00dba-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00dba-144">產品</span><span class="sxs-lookup"><span data-stu-id="00dba-144">Product</span></span><br/>                  | <span data-ttu-id="00dba-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00dba-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00dba-146">標頭</span><span class="sxs-lookup"><span data-stu-id="00dba-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="00dba-147"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="00dba-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00dba-148">IID</span><span class="sxs-lookup"><span data-stu-id="00dba-148">IID</span></span><br/>                      | <span data-ttu-id="00dba-149">IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="00dba-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="00dba-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00dba-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00dba-151">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="00dba-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

