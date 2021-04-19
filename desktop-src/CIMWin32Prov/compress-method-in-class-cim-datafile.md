---
description: 使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: fce57569-8290-420e-a938-10ab08ac67c3
ms.tgt_platform: multiple
title: 壓縮 CIM_DataFile 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99d9a0a346d8a9394edd9f30ff23490549f6de76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967034"
---
# <a name="compress-method-of-the-cim_datafile-class"></a><span data-ttu-id="b8a7e-104">壓縮 CIM \_ 資料檔案類別的方法</span><span class="sxs-lookup"><span data-stu-id="b8a7e-104">Compress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b8a7e-105">**壓縮** 方法會使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-105">The **Compress** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="b8a7e-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8a7e-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8a7e-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8a7e-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b8a7e-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a7e-111">語法</span><span class="sxs-lookup"><span data-stu-id="b8a7e-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="b8a7e-112">參數</span><span class="sxs-lookup"><span data-stu-id="b8a7e-112">Parameters</span></span>

<span data-ttu-id="b8a7e-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8a7e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8a7e-114">Return value</span></span>

<span data-ttu-id="b8a7e-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b8a7e-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b8a7e-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b8a7e-118">**0**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-119">成功。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-120">**2**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-122">**8**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-123">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-124">**9**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-125">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-126">**10**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-127">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-128">**11**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-129">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-130">**12**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-131">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-132">**13**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-133">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-134">**14**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-135">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-136">**15**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-137">共用違規。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-138">**16**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-139">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-140">**17**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-141">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7e-142">**21**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b8a7e-143">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8a7e-144">備註</span><span class="sxs-lookup"><span data-stu-id="b8a7e-144">Remarks</span></span>

<span data-ttu-id="b8a7e-145">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **壓縮** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-145">The **Compress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b8a7e-146">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8a7e-147">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b8a7e-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a7e-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a7e-148">Requirements</span></span>



| <span data-ttu-id="b8a7e-149">需求</span><span class="sxs-lookup"><span data-stu-id="b8a7e-149">Requirement</span></span> | <span data-ttu-id="b8a7e-150">值</span><span class="sxs-lookup"><span data-stu-id="b8a7e-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a7e-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8a7e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a7e-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8a7e-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8a7e-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8a7e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a7e-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8a7e-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8a7e-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8a7e-155">Namespace</span></span><br/>                | <span data-ttu-id="b8a7e-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8a7e-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8a7e-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b8a7e-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8a7e-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8a7e-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8a7e-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a7e-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a7e-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8a7e-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a7e-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8a7e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a7e-162">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-162">**CIM\_DataFile**</span></span>](compress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b8a7e-163">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b8a7e-164">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="b8a7e-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b8a7e-165">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="b8a7e-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

