---
title: 'IVMSerialPortCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內序列埠的集合。 若要取得 IVMSerialPortCollection 物件，請使用 IVMVirtualMachine Serialport 屬性。
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- IVMSerialPortCollection 介面 Virtual PC
- IVMSerialPortCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685967"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="5c5a3-106">IVMSerialPortCollection 介面</span><span class="sxs-lookup"><span data-stu-id="5c5a3-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="5c5a3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5c5a3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5c5a3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5c5a3-109">定義虛擬機器內序列埠的集合。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="5c5a3-110">若要取得 **IVMSerialPortCollection** 物件，請使用 [**IVMVirtualMachine：： serialport**](ivmvirtualmachine-serialports.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="5c5a3-111">成員</span><span class="sxs-lookup"><span data-stu-id="5c5a3-111">Members</span></span>

<span data-ttu-id="5c5a3-112">**IVMSerialPortCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5c5a3-113">**IVMSerialPortCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5c5a3-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="5c5a3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5c5a3-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c5a3-115">屬性</span><span class="sxs-lookup"><span data-stu-id="5c5a3-115">Properties</span></span>

<span data-ttu-id="5c5a3-116">**IVMSerialPortCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="5c5a3-117">屬性</span><span class="sxs-lookup"><span data-stu-id="5c5a3-117">Property</span></span>                                                         | <span data-ttu-id="5c5a3-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="5c5a3-118">Access type</span></span>          | <span data-ttu-id="5c5a3-119">Description</span><span class="sxs-lookup"><span data-stu-id="5c5a3-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="5c5a3-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5c5a3-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="5c5a3-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="5c5a3-121">Read-only</span></span><br/> | <span data-ttu-id="5c5a3-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="5c5a3-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="5c5a3-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="5c5a3-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="5c5a3-124">Read-only</span></span><br/> | <span data-ttu-id="5c5a3-125">此集合中的序列埠數目。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="5c5a3-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="5c5a3-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="5c5a3-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="5c5a3-127">Read-only</span></span><br/> | <span data-ttu-id="5c5a3-128">對應至指定之索引的序列通訊埠物件。</span><span class="sxs-lookup"><span data-stu-id="5c5a3-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5c5a3-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c5a3-129">Requirements</span></span>



| <span data-ttu-id="5c5a3-130">需求</span><span class="sxs-lookup"><span data-stu-id="5c5a3-130">Requirement</span></span> | <span data-ttu-id="5c5a3-131">值</span><span class="sxs-lookup"><span data-stu-id="5c5a3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5a3-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c5a3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5a3-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c5a3-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c5a3-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c5a3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5a3-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c5a3-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5c5a3-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5c5a3-136">End of client support</span></span><br/>    | <span data-ttu-id="5c5a3-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c5a3-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5c5a3-138">產品</span><span class="sxs-lookup"><span data-stu-id="5c5a3-138">Product</span></span><br/>                  | <span data-ttu-id="5c5a3-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5c5a3-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5c5a3-140">標頭</span><span class="sxs-lookup"><span data-stu-id="5c5a3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c5a3-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c5a3-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5c5a3-142">IID</span><span class="sxs-lookup"><span data-stu-id="5c5a3-142">IID</span></span><br/>                      | <span data-ttu-id="5c5a3-143">IID \_ IVMSerialPortCollection 定義為 dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="5c5a3-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="5c5a3-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c5a3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5a3-145">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="5c5a3-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="5c5a3-146">**IVMVirtualMachine：： Serialport**</span><span class="sxs-lookup"><span data-stu-id="5c5a3-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

