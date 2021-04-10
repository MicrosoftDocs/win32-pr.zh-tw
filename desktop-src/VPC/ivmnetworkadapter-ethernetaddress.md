---
title: 'IVMNetworkAdapter EthernetAddress 屬性 (VPCCOMInterfaces .h) '
description: 網路介面的乙太網路 (MAC) 位址。
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- EthernetAddress 屬性 Virtual PC
- EthernetAddress 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，EthernetAddress 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685472"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="e9ca2-106">IVMNetworkAdapter：： EthernetAddress 屬性</span><span class="sxs-lookup"><span data-stu-id="e9ca2-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="e9ca2-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e9ca2-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e9ca2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e9ca2-109">抓取並設定網路介面的 Ethernet (MAC) 位址。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="e9ca2-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ca2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9ca2-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="e9ca2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9ca2-112">Property value</span></span>

<span data-ttu-id="e9ca2-113">虛擬 NIC 的 MAC 位址。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="e9ca2-114">它的格式應該是「*xx* xx xx xx xx xx」 -  -  -  -  - \*\*，其中每個 *X* 都是十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e9ca2-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e9ca2-115">Error codes</span></span>



| <span data-ttu-id="e9ca2-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="e9ca2-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="e9ca2-117">意義</span><span class="sxs-lookup"><span data-stu-id="e9ca2-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9ca2-118"><dt>S \_ 確定</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="e9ca2-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="e9ca2-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="e9ca2-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e9ca2-122"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="e9ca2-123">參數的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="e9ca2-124"><dt>VM \_E \_ 無法 \_ 設定 \_ 動態 \_ MAC \_ 位址</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="e9ca2-125">網路介面的乙太網路位址可以動態產生，也可以由使用者設定為靜態位址。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="e9ca2-126">當地址設定為動態產生時，無法呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="e9ca2-127">[**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)屬性是用來變更乙太網路位址的產生行為。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="e9ca2-128"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="e9ca2-129">找不到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-129">The virtual machine was not found.</span></span> <span data-ttu-id="e9ca2-130">如果在建立 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件之後移除電腦，就可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="e9ca2-131"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="e9ca2-132">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9ca2-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="e9ca2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9ca2-133">Requirements</span></span>



| <span data-ttu-id="e9ca2-134">需求</span><span class="sxs-lookup"><span data-stu-id="e9ca2-134">Requirement</span></span> | <span data-ttu-id="e9ca2-135">值</span><span class="sxs-lookup"><span data-stu-id="e9ca2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ca2-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9ca2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ca2-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9ca2-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e9ca2-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9ca2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ca2-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="e9ca2-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e9ca2-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e9ca2-140">End of client support</span></span><br/>    | <span data-ttu-id="e9ca2-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9ca2-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e9ca2-142">產品</span><span class="sxs-lookup"><span data-stu-id="e9ca2-142">Product</span></span><br/>                  | <span data-ttu-id="e9ca2-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e9ca2-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e9ca2-144">標頭</span><span class="sxs-lookup"><span data-stu-id="e9ca2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ca2-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ca2-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e9ca2-146">IID</span><span class="sxs-lookup"><span data-stu-id="e9ca2-146">IID</span></span><br/>                      | <span data-ttu-id="e9ca2-147">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="e9ca2-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e9ca2-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ca2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ca2-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="e9ca2-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

