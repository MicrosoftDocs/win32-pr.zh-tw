---
title: 'IVMSerialPort 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的序列埠。
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- IVMSerialPort 介面 Virtual PC
- IVMSerialPort 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508987"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="06091-105">IVMSerialPort 介面</span><span class="sxs-lookup"><span data-stu-id="06091-105">IVMSerialPort interface</span></span>

<span data-ttu-id="06091-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="06091-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="06091-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="06091-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="06091-108">定義虛擬機器內的序列埠。</span><span class="sxs-lookup"><span data-stu-id="06091-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="06091-109">此介面可讓您設定虛擬機器內的序列埠。</span><span class="sxs-lookup"><span data-stu-id="06091-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="06091-110">您可以從 [**IVMVirtualMachine：： serialport**](ivmvirtualmachine-serialports.md)屬性傳回的 [**IVMSerialPortCollection**](ivmserialportcollection.md)物件中取出 **IVMSerialPort** 物件。</span><span class="sxs-lookup"><span data-stu-id="06091-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="06091-111">成員</span><span class="sxs-lookup"><span data-stu-id="06091-111">Members</span></span>

<span data-ttu-id="06091-112">**IVMSerialPort** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="06091-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="06091-113">**IVMSerialPort** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="06091-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="06091-114">方法</span><span class="sxs-lookup"><span data-stu-id="06091-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="06091-115">屬性</span><span class="sxs-lookup"><span data-stu-id="06091-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06091-116">方法</span><span class="sxs-lookup"><span data-stu-id="06091-116">Methods</span></span>

<span data-ttu-id="06091-117">**IVMSerialPort** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="06091-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="06091-118">方法</span><span class="sxs-lookup"><span data-stu-id="06091-118">Method</span></span>                                       | <span data-ttu-id="06091-119">描述</span><span class="sxs-lookup"><span data-stu-id="06091-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="06091-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="06091-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="06091-121">捕獲序列埠的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="06091-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="06091-122">**設定**</span><span class="sxs-lookup"><span data-stu-id="06091-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="06091-123">設定序列埠。</span><span class="sxs-lookup"><span data-stu-id="06091-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="06091-124">屬性</span><span class="sxs-lookup"><span data-stu-id="06091-124">Properties</span></span>

<span data-ttu-id="06091-125">**IVMSerialPort** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="06091-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="06091-126">屬性</span><span class="sxs-lookup"><span data-stu-id="06091-126">Property</span></span>                                                                  | <span data-ttu-id="06091-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="06091-127">Access type</span></span>          | <span data-ttu-id="06091-128">Description</span><span class="sxs-lookup"><span data-stu-id="06091-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06091-129">**ConnectImmediately**</span><span class="sxs-lookup"><span data-stu-id="06091-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="06091-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="06091-130">Read-only</span></span><br/> | <span data-ttu-id="06091-131">指出是否應該在不等候數據機命令的情況下開啟序列埠。</span><span class="sxs-lookup"><span data-stu-id="06091-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="06091-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="06091-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="06091-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="06091-133">Read-only</span></span><br/> | <span data-ttu-id="06091-134">序列埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="06091-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="06091-135">**類型**</span><span class="sxs-lookup"><span data-stu-id="06091-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="06091-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="06091-136">Read-only</span></span><br/> | <span data-ttu-id="06091-137">序列埠的型別。</span><span class="sxs-lookup"><span data-stu-id="06091-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="06091-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="06091-138">Requirements</span></span>



| <span data-ttu-id="06091-139">需求</span><span class="sxs-lookup"><span data-stu-id="06091-139">Requirement</span></span> | <span data-ttu-id="06091-140">值</span><span class="sxs-lookup"><span data-stu-id="06091-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06091-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06091-141">Minimum supported client</span></span><br/> | <span data-ttu-id="06091-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06091-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06091-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06091-143">Minimum supported server</span></span><br/> | <span data-ttu-id="06091-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="06091-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="06091-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="06091-145">End of client support</span></span><br/>    | <span data-ttu-id="06091-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06091-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="06091-147">產品</span><span class="sxs-lookup"><span data-stu-id="06091-147">Product</span></span><br/>                  | <span data-ttu-id="06091-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="06091-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="06091-149">標頭</span><span class="sxs-lookup"><span data-stu-id="06091-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="06091-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="06091-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="06091-151">IID</span><span class="sxs-lookup"><span data-stu-id="06091-151">IID</span></span><br/>                      | <span data-ttu-id="06091-152">IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="06091-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

