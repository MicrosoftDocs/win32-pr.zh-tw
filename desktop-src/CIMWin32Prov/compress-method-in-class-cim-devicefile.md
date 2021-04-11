---
description: 壓縮方法會將邏輯檔案壓縮 (或在物件路徑中指定的目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: baafe82c-fe4d-49b2-8868-4495f573895a
ms.tgt_platform: multiple
title: 壓縮 CIM_DeviceFile 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0af6a1792383ad2665064a6e577807997a1aba16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847097"
---
# <a name="compress-method-of-the-cim_devicefile-class"></a><span data-ttu-id="8a708-104">壓縮 CIM \_ DeviceFile 類別的方法</span><span class="sxs-lookup"><span data-stu-id="8a708-104">Compress method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="8a708-105">**壓縮** 方法會將邏輯檔案壓縮 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="8a708-105">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="8a708-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="8a708-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a708-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8a708-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8a708-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8a708-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8a708-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8a708-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8a708-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8a708-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a708-111">語法</span><span class="sxs-lookup"><span data-stu-id="8a708-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="8a708-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a708-112">Parameters</span></span>

<span data-ttu-id="8a708-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8a708-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a708-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a708-114">Return value</span></span>

<span data-ttu-id="8a708-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8a708-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8a708-116">**0**</span><span class="sxs-lookup"><span data-stu-id="8a708-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-117">成功。</span><span class="sxs-lookup"><span data-stu-id="8a708-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-118">**2**</span><span class="sxs-lookup"><span data-stu-id="8a708-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-119">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8a708-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-120">**8**</span><span class="sxs-lookup"><span data-stu-id="8a708-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-121">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="8a708-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-122">**9**</span><span class="sxs-lookup"><span data-stu-id="8a708-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-123">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="8a708-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-124">**10**</span><span class="sxs-lookup"><span data-stu-id="8a708-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-125">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="8a708-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-126">**11**</span><span class="sxs-lookup"><span data-stu-id="8a708-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-127">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="8a708-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-128">**12**</span><span class="sxs-lookup"><span data-stu-id="8a708-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-129">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="8a708-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-130">**13**</span><span class="sxs-lookup"><span data-stu-id="8a708-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-131">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="8a708-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-132">**14**</span><span class="sxs-lookup"><span data-stu-id="8a708-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-133">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="8a708-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-134">**15**</span><span class="sxs-lookup"><span data-stu-id="8a708-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-135">共用違規。</span><span class="sxs-lookup"><span data-stu-id="8a708-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-136">**16**</span><span class="sxs-lookup"><span data-stu-id="8a708-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-137">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="8a708-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-138">**17**</span><span class="sxs-lookup"><span data-stu-id="8a708-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-139">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="8a708-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="8a708-140">**21**</span><span class="sxs-lookup"><span data-stu-id="8a708-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8a708-141">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="8a708-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a708-142">備註</span><span class="sxs-lookup"><span data-stu-id="8a708-142">Remarks</span></span>

<span data-ttu-id="8a708-143">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="8a708-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8a708-144">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="8a708-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8a708-145">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8a708-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8a708-146">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8a708-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a708-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a708-147">Requirements</span></span>



| <span data-ttu-id="8a708-148">需求</span><span class="sxs-lookup"><span data-stu-id="8a708-148">Requirement</span></span> | <span data-ttu-id="8a708-149">值</span><span class="sxs-lookup"><span data-stu-id="8a708-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a708-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a708-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8a708-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a708-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a708-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a708-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8a708-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a708-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a708-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a708-154">Namespace</span></span><br/>                | <span data-ttu-id="8a708-155">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8a708-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8a708-156">MOF</span><span class="sxs-lookup"><span data-stu-id="8a708-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a708-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a708-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a708-158">DLL</span><span class="sxs-lookup"><span data-stu-id="8a708-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a708-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a708-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a708-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a708-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a708-161">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="8a708-161">CIM\_DeviceFile</span></span>](compress-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="8a708-162">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="8a708-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

