---
description: Uncompresses 邏輯資料檔案 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111393"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="695e3-104">CIM \_ 資料檔案類別的 UncompressEx 方法</span><span class="sxs-lookup"><span data-stu-id="695e3-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="695e3-105">**UncompressEx** 方法會 uncompresses 物件路徑中指定的邏輯資料檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="695e3-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="695e3-106">這個方法是 [**解壓縮**](uncompress-method-in-class-cim-datafile.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="695e3-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="695e3-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="695e3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="695e3-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="695e3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="695e3-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="695e3-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="695e3-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="695e3-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="695e3-111">語法</span><span class="sxs-lookup"><span data-stu-id="695e3-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="695e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="695e3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695e3-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="695e3-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="695e3-114">方法失敗 (或目錄) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="695e3-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="695e3-115">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="695e3-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-116">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="695e3-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695e3-117">要做為這個方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="695e3-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="695e3-118">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="695e3-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="695e3-119">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="695e3-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="695e3-120">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="695e3-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-121">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="695e3-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695e3-122">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="695e3-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="695e3-123">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="695e3-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695e3-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="695e3-124">Return value</span></span>

<span data-ttu-id="695e3-125">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="695e3-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="695e3-126">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="695e3-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="695e3-127">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="695e3-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="695e3-128">**0**</span><span class="sxs-lookup"><span data-stu-id="695e3-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-129">成功。</span><span class="sxs-lookup"><span data-stu-id="695e3-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-130">**2**</span><span class="sxs-lookup"><span data-stu-id="695e3-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-131">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="695e3-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-132">**8**</span><span class="sxs-lookup"><span data-stu-id="695e3-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-133">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="695e3-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-134">**9**</span><span class="sxs-lookup"><span data-stu-id="695e3-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-135">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="695e3-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-136">**10**</span><span class="sxs-lookup"><span data-stu-id="695e3-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-137">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="695e3-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-138">**11**</span><span class="sxs-lookup"><span data-stu-id="695e3-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-139">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="695e3-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-140">**12**</span><span class="sxs-lookup"><span data-stu-id="695e3-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-141">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="695e3-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-142">**13**</span><span class="sxs-lookup"><span data-stu-id="695e3-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-143">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="695e3-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-144">**14**</span><span class="sxs-lookup"><span data-stu-id="695e3-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-145">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="695e3-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-146">**15**</span><span class="sxs-lookup"><span data-stu-id="695e3-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-147">共用違規。</span><span class="sxs-lookup"><span data-stu-id="695e3-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-148">**16**</span><span class="sxs-lookup"><span data-stu-id="695e3-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-149">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="695e3-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-150">**17**</span><span class="sxs-lookup"><span data-stu-id="695e3-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-151">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="695e3-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="695e3-152">**21**</span><span class="sxs-lookup"><span data-stu-id="695e3-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="695e3-153">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="695e3-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="695e3-154">備註</span><span class="sxs-lookup"><span data-stu-id="695e3-154">Remarks</span></span>

<span data-ttu-id="695e3-155">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **UNCOMPRESSEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="695e3-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="695e3-156">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="695e3-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="695e3-157">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="695e3-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="695e3-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="695e3-158">Requirements</span></span>



| <span data-ttu-id="695e3-159">需求</span><span class="sxs-lookup"><span data-stu-id="695e3-159">Requirement</span></span> | <span data-ttu-id="695e3-160">值</span><span class="sxs-lookup"><span data-stu-id="695e3-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="695e3-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="695e3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="695e3-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="695e3-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="695e3-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="695e3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="695e3-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="695e3-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="695e3-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="695e3-165">Namespace</span></span><br/>                | <span data-ttu-id="695e3-166">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="695e3-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="695e3-167">MOF</span><span class="sxs-lookup"><span data-stu-id="695e3-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="695e3-168"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="695e3-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="695e3-169">DLL</span><span class="sxs-lookup"><span data-stu-id="695e3-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="695e3-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="695e3-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="695e3-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="695e3-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695e3-172">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="695e3-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="695e3-173">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="695e3-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="695e3-174">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="695e3-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="695e3-175">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="695e3-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

