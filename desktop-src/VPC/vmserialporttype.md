---
title: 'VMSerialPortType 列舉 (VPCCOMInterfaces) '
description: 指定序列埠的類型。
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- VMSerialPortType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508971"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="d3360-104">VMSerialPortType 列舉</span><span class="sxs-lookup"><span data-stu-id="d3360-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="d3360-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="d3360-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3360-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="d3360-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3360-107">指定序列埠的類型。</span><span class="sxs-lookup"><span data-stu-id="d3360-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3360-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3360-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="d3360-109">常數</span><span class="sxs-lookup"><span data-stu-id="d3360-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d3360-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort \_ HostPort**</span><span class="sxs-lookup"><span data-stu-id="d3360-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="d3360-111">主機序列埠。</span><span class="sxs-lookup"><span data-stu-id="d3360-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="d3360-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort \_ TextFile**</span><span class="sxs-lookup"><span data-stu-id="d3360-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="d3360-113">主機文字檔。</span><span class="sxs-lookup"><span data-stu-id="d3360-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="d3360-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="d3360-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="d3360-115">具名管道。</span><span class="sxs-lookup"><span data-stu-id="d3360-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="d3360-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort \_ Null**</span><span class="sxs-lookup"><span data-stu-id="d3360-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="d3360-117">**Null** 序列埠 (捨棄傳送給它) 的所有位。</span><span class="sxs-lookup"><span data-stu-id="d3360-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3360-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3360-118">Requirements</span></span>



| <span data-ttu-id="d3360-119">需求</span><span class="sxs-lookup"><span data-stu-id="d3360-119">Requirement</span></span> | <span data-ttu-id="d3360-120">值</span><span class="sxs-lookup"><span data-stu-id="d3360-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3360-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3360-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d3360-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3360-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3360-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3360-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d3360-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="d3360-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3360-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d3360-125">End of client support</span></span><br/>    | <span data-ttu-id="d3360-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3360-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3360-127">產品</span><span class="sxs-lookup"><span data-stu-id="d3360-127">Product</span></span><br/>                  | <span data-ttu-id="d3360-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3360-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3360-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d3360-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3360-130"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3360-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3360-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3360-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3360-132">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="d3360-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

