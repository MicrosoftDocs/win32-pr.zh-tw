---
description: CIM_DataFile 類別的 CompressEx 方法-使用 NTFS 壓縮來壓縮物件路徑中所指定的邏輯檔案 (或目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 CompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089786"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="2e01d-104">CIM \_ 資料檔案類別的 CompressEx 方法</span><span class="sxs-lookup"><span data-stu-id="2e01d-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2e01d-105">**CompressEx** 方法會使用 NTFS 壓縮來壓縮物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="2e01d-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="2e01d-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="2e01d-107">這個方法是 [**壓縮**](compress-method-in-class-cim-datafile.md) 方法的擴充版本，會繼承自 [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e01d-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2e01d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e01d-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e01d-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2e01d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e01d-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e01d-112">語法</span><span class="sxs-lookup"><span data-stu-id="2e01d-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2e01d-113">參數</span><span class="sxs-lookup"><span data-stu-id="2e01d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e01d-114">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2e01d-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-115">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e01d-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2e01d-116">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="2e01d-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-117">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e01d-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-118">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="2e01d-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2e01d-119">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="2e01d-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2e01d-120">如果這個參數是 null，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="2e01d-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="2e01d-121">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="2e01d-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-122">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e01d-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-123">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="2e01d-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="2e01d-124">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="2e01d-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e01d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e01d-125">Return value</span></span>

<span data-ttu-id="2e01d-126">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e01d-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2e01d-127">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e01d-128">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="2e01d-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e01d-129">**0**</span><span class="sxs-lookup"><span data-stu-id="2e01d-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-130">成功。</span><span class="sxs-lookup"><span data-stu-id="2e01d-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-131">**2**</span><span class="sxs-lookup"><span data-stu-id="2e01d-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-132">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="2e01d-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-133">**8**</span><span class="sxs-lookup"><span data-stu-id="2e01d-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-134">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="2e01d-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-135">**9**</span><span class="sxs-lookup"><span data-stu-id="2e01d-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-136">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="2e01d-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-137">**10**</span><span class="sxs-lookup"><span data-stu-id="2e01d-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-138">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="2e01d-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-139">**11**</span><span class="sxs-lookup"><span data-stu-id="2e01d-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-140">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="2e01d-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-141">**12**</span><span class="sxs-lookup"><span data-stu-id="2e01d-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-142">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="2e01d-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-143">**13**</span><span class="sxs-lookup"><span data-stu-id="2e01d-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-144">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="2e01d-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-145">**14**</span><span class="sxs-lookup"><span data-stu-id="2e01d-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-146">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="2e01d-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-147">**15**</span><span class="sxs-lookup"><span data-stu-id="2e01d-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-148">共用違規。</span><span class="sxs-lookup"><span data-stu-id="2e01d-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-149">**16**</span><span class="sxs-lookup"><span data-stu-id="2e01d-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-150">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="2e01d-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-151">**17**</span><span class="sxs-lookup"><span data-stu-id="2e01d-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-152">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="2e01d-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2e01d-153">**21**</span><span class="sxs-lookup"><span data-stu-id="2e01d-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2e01d-154">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="2e01d-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e01d-155">備註</span><span class="sxs-lookup"><span data-stu-id="2e01d-155">Remarks</span></span>

<span data-ttu-id="2e01d-156">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **COMPRESSEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2e01d-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2e01d-157">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2e01d-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e01d-158">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2e01d-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e01d-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e01d-159">Requirements</span></span>



| <span data-ttu-id="2e01d-160">需求</span><span class="sxs-lookup"><span data-stu-id="2e01d-160">Requirement</span></span> | <span data-ttu-id="2e01d-161">值</span><span class="sxs-lookup"><span data-stu-id="2e01d-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e01d-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e01d-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2e01d-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e01d-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e01d-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e01d-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2e01d-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e01d-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e01d-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="2e01d-166">Namespace</span></span><br/>                | <span data-ttu-id="2e01d-167">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e01d-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e01d-168">MOF</span><span class="sxs-lookup"><span data-stu-id="2e01d-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e01d-169"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e01d-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e01d-170">DLL</span><span class="sxs-lookup"><span data-stu-id="2e01d-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e01d-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e01d-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e01d-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e01d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e01d-173">CIM \_ 資料檔案</span><span class="sxs-lookup"><span data-stu-id="2e01d-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e01d-174">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="2e01d-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e01d-175">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="2e01d-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2e01d-176">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="2e01d-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

