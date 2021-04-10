---
description: GetDescriptor 方法會傳回輸入參數所指定的 USB 中樞描述元。
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: 'CIM_USBHub 類別的 GetDescriptor 方法 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936218"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="9721d-103">CIM USBHub 類別的 GetDescriptor 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9721d-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="9721d-104">**GetDescriptor** 方法會傳回輸入參數所指定的 USB 中樞描述元。</span><span class="sxs-lookup"><span data-stu-id="9721d-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9721d-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9721d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9721d-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9721d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9721d-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="9721d-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9721d-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="9721d-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9721d-109">語法</span><span class="sxs-lookup"><span data-stu-id="9721d-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="9721d-110">參數</span><span class="sxs-lookup"><span data-stu-id="9721d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9721d-111">*RequestType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9721d-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9721d-112">描述項要求類型和收件者的位對應識別碼。</span><span class="sxs-lookup"><span data-stu-id="9721d-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="9721d-113">如需每個位的適當值，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="9721d-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9721d-114">*RequestValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9721d-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9721d-115">包含在高位元組和描述元索引中的描述元類型 (例如，在低位元組中的描述元陣列) 的索引或位移。</span><span class="sxs-lookup"><span data-stu-id="9721d-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="9721d-116">如需詳細資訊，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="9721d-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9721d-117">*RequestIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9721d-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9721d-118">指定傳回字串描述中繼資料時，USB 裝置所使用的2位元組語言識別項程式碼。</span><span class="sxs-lookup"><span data-stu-id="9721d-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="9721d-119">參數通常是非字串描述項的 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="9721d-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="9721d-120">如需詳細資訊，請參閱 USB 規格。</span><span class="sxs-lookup"><span data-stu-id="9721d-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="9721d-121">*RequestLength* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="9721d-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9721d-122">在輸入時，長度會 (為應傳回之描述項的八位) 。</span><span class="sxs-lookup"><span data-stu-id="9721d-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="9721d-123">如果這個值小於描述項的實際長度，則只會傳回要求的長度。</span><span class="sxs-lookup"><span data-stu-id="9721d-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="9721d-124">如果超過實際的長度，則會傳回實際長度。</span><span class="sxs-lookup"><span data-stu-id="9721d-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="9721d-125">在輸出時，長度會在傳回的緩衝區中，以八位)  (。</span><span class="sxs-lookup"><span data-stu-id="9721d-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="9721d-126">如果要求的描述項不存在，則此參數的內容為未定義。</span><span class="sxs-lookup"><span data-stu-id="9721d-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9721d-127">*緩衝區* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9721d-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9721d-128">Buffer 會傳回要求的描述項資訊。</span><span class="sxs-lookup"><span data-stu-id="9721d-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="9721d-129">如果描述項不存在，則會未定義緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="9721d-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9721d-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="9721d-130">Return value</span></span>

<span data-ttu-id="9721d-131">如果成功傳回 USB 描述項，則傳回 0 (零) 的值，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="9721d-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="9721d-132">在子類別中，可能會使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="9721d-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="9721d-133">要轉譯 **mofqualifier** 內容的字串，也可以在子類別中指定為 **值** 陣列限定詞。</span><span class="sxs-lookup"><span data-stu-id="9721d-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="9721d-134">備註</span><span class="sxs-lookup"><span data-stu-id="9721d-134">Remarks</span></span>

<span data-ttu-id="9721d-135">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="9721d-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9721d-136">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="9721d-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9721d-137">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9721d-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9721d-138">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9721d-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9721d-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="9721d-139">Requirements</span></span>



| <span data-ttu-id="9721d-140">需求</span><span class="sxs-lookup"><span data-stu-id="9721d-140">Requirement</span></span> | <span data-ttu-id="9721d-141">值</span><span class="sxs-lookup"><span data-stu-id="9721d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9721d-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9721d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9721d-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9721d-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9721d-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9721d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9721d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9721d-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9721d-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="9721d-146">Namespace</span></span><br/>                | <span data-ttu-id="9721d-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9721d-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9721d-148">標頭</span><span class="sxs-lookup"><span data-stu-id="9721d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="9721d-149"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9721d-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9721d-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9721d-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9721d-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9721d-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9721d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9721d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9721d-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9721d-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9721d-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9721d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9721d-155">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="9721d-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="9721d-156">**CIM \_ USBHub**</span><span class="sxs-lookup"><span data-stu-id="9721d-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

