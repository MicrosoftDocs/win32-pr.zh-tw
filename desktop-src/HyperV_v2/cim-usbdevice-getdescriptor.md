---
description: 傳回輸入參數所指定的 USBDevice 描述元。
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: 'CIM_USBDevice 類別的 GetDescriptor 方法 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977857"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="2d67c-103">CIM_USBDevice 類別的 GetDescriptor 方法 (Hyper-v 管理) </span><span class="sxs-lookup"><span data-stu-id="2d67c-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="2d67c-104">傳回輸入參數所指定的 USBDevice 描述元。</span><span class="sxs-lookup"><span data-stu-id="2d67c-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d67c-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d67c-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="2d67c-106">參數</span><span class="sxs-lookup"><span data-stu-id="2d67c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d67c-107">*RequestType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d67c-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d67c-108">識別描述項要求類型和收件者的位對應。</span><span class="sxs-lookup"><span data-stu-id="2d67c-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="2d67c-109">要求的類型可能是「標準」、「類別」或「供應商特定」。</span><span class="sxs-lookup"><span data-stu-id="2d67c-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="2d67c-110">收件者可以是「裝置」、「介面」、「端點」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="2d67c-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="2d67c-111">請參閱 USB 規格，以取得每個位的適當值。</span><span class="sxs-lookup"><span data-stu-id="2d67c-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="2d67c-112">*RequestValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d67c-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d67c-113">包含在高位元組和描述元索引中的描述元類型 (例如，在低位元組中的描述元陣列) 的索引或位移。</span><span class="sxs-lookup"><span data-stu-id="2d67c-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="2d67c-114">如需詳細資訊，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="2d67c-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="2d67c-115">*RequestIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d67c-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d67c-116">定義傳回字串描述中繼資料時，USBDevice 所使用的2位元組語言識別項程式碼。</span><span class="sxs-lookup"><span data-stu-id="2d67c-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="2d67c-117">非字串描述項的參數通常是0。</span><span class="sxs-lookup"><span data-stu-id="2d67c-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="2d67c-118">如需詳細資訊，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="2d67c-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="2d67c-119">*RequestLength* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2d67c-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d67c-120">在輸入上，包含應傳回之描述項的長度 (以八位) 。</span><span class="sxs-lookup"><span data-stu-id="2d67c-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="2d67c-121">如果這個值小於描述項的實際長度，則只會傳回要求的長度。</span><span class="sxs-lookup"><span data-stu-id="2d67c-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="2d67c-122">如果超過實際的長度，則會傳回實際長度。</span><span class="sxs-lookup"><span data-stu-id="2d67c-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="2d67c-123">在輸出中，這個參數是要傳回之緩衝區的長度（以八位）。</span><span class="sxs-lookup"><span data-stu-id="2d67c-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="2d67c-124">如果要求的描述項不存在，則此參數的內容為未定義。</span><span class="sxs-lookup"><span data-stu-id="2d67c-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="2d67c-125">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2d67c-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d67c-126">傳回要求的描述項資訊。</span><span class="sxs-lookup"><span data-stu-id="2d67c-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="2d67c-127">如果描述項不存在，則參數的內容為未定義。</span><span class="sxs-lookup"><span data-stu-id="2d67c-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d67c-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d67c-128">Return value</span></span>

<span data-ttu-id="2d67c-129">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2d67c-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d67c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d67c-130">Requirements</span></span>



| <span data-ttu-id="2d67c-131">需求</span><span class="sxs-lookup"><span data-stu-id="2d67c-131">Requirement</span></span> | <span data-ttu-id="2d67c-132">值</span><span class="sxs-lookup"><span data-stu-id="2d67c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d67c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d67c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2d67c-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2d67c-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2d67c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d67c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2d67c-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2d67c-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2d67c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2d67c-137">Namespace</span></span><br/>                | <span data-ttu-id="2d67c-138">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2d67c-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2d67c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2d67c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d67c-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2d67c-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d67c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2d67c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d67c-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d67c-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d67c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d67c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d67c-144">**CIM \_ USBDevice**</span><span class="sxs-lookup"><span data-stu-id="2d67c-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




