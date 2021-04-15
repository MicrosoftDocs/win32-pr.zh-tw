---
description: 取得物件路徑中所指定之邏輯資料檔案的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: 3bc5a060-d805-46f6-802d-9ed16b52da59
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 41124567e8743227f46c9cb3b84dcb0d1f788bc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468445"
---
# <a name="takeownershipex-method-of-the-cim_datafile-class"></a><span data-ttu-id="55ed5-104">CIM \_ 資料檔案類別的 TakeOwnerShipEx 方法</span><span class="sxs-lookup"><span data-stu-id="55ed5-104">TakeOwnerShipEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="55ed5-105">**TakeOwnerShipEx** 方法會取得物件路徑中所指定之邏輯資料檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="55ed5-105">The **TakeOwnerShipEx** method obtains ownership of the logical data file that is specified in the object path.</span></span> <span data-ttu-id="55ed5-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="55ed5-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="55ed5-107">如果邏輯檔案是目錄，則此方法會以遞迴方式執行，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="55ed5-107">If the logical file is a directory, then this method will act recursively, taking ownership of all files and subdirectories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55ed5-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="55ed5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55ed5-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="55ed5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55ed5-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="55ed5-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55ed5-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="55ed5-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55ed5-112">語法</span><span class="sxs-lookup"><span data-stu-id="55ed5-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="55ed5-113">參數</span><span class="sxs-lookup"><span data-stu-id="55ed5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ed5-114">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55ed5-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-115">方法失敗 (或目錄) 的檔案名。</span><span class="sxs-lookup"><span data-stu-id="55ed5-115">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="55ed5-116">如果方法成功，此參數將會是 null。</span><span class="sxs-lookup"><span data-stu-id="55ed5-116">This parameter will be null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-117">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55ed5-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-118">要做為這個方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="55ed5-118">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="55ed5-119">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="55ed5-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="55ed5-120">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="55ed5-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="55ed5-121">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="55ed5-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-122">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55ed5-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-123">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="55ed5-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="55ed5-124">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="55ed5-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ed5-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="55ed5-125">Return value</span></span>

<span data-ttu-id="55ed5-126">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="55ed5-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="55ed5-127">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="55ed5-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="55ed5-128">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="55ed5-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="55ed5-129">**0**</span><span class="sxs-lookup"><span data-stu-id="55ed5-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-130">成功。</span><span class="sxs-lookup"><span data-stu-id="55ed5-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-131">**2**</span><span class="sxs-lookup"><span data-stu-id="55ed5-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-132">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="55ed5-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-133">**8**</span><span class="sxs-lookup"><span data-stu-id="55ed5-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-134">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="55ed5-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-135">**9**</span><span class="sxs-lookup"><span data-stu-id="55ed5-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-136">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="55ed5-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-137">**10**</span><span class="sxs-lookup"><span data-stu-id="55ed5-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-138">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="55ed5-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-139">**11**</span><span class="sxs-lookup"><span data-stu-id="55ed5-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-140">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="55ed5-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-141">**12**</span><span class="sxs-lookup"><span data-stu-id="55ed5-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-142">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="55ed5-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-143">**13**</span><span class="sxs-lookup"><span data-stu-id="55ed5-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-144">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="55ed5-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-145">**14**</span><span class="sxs-lookup"><span data-stu-id="55ed5-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-146">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="55ed5-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-147">**15**</span><span class="sxs-lookup"><span data-stu-id="55ed5-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-148">共用違規。</span><span class="sxs-lookup"><span data-stu-id="55ed5-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-149">**16**</span><span class="sxs-lookup"><span data-stu-id="55ed5-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-150">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="55ed5-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-151">**17**</span><span class="sxs-lookup"><span data-stu-id="55ed5-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-152">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="55ed5-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="55ed5-153">**21**</span><span class="sxs-lookup"><span data-stu-id="55ed5-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="55ed5-154">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="55ed5-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55ed5-155">備註</span><span class="sxs-lookup"><span data-stu-id="55ed5-155">Remarks</span></span>

<span data-ttu-id="55ed5-156">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **TAKEOWNERSHIPEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="55ed5-156">The **TakeOwnerShipEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="55ed5-157">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="55ed5-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55ed5-158">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="55ed5-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ed5-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="55ed5-159">Requirements</span></span>



| <span data-ttu-id="55ed5-160">需求</span><span class="sxs-lookup"><span data-stu-id="55ed5-160">Requirement</span></span> | <span data-ttu-id="55ed5-161">值</span><span class="sxs-lookup"><span data-stu-id="55ed5-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55ed5-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55ed5-162">Minimum supported client</span></span><br/> | <span data-ttu-id="55ed5-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55ed5-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55ed5-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55ed5-164">Minimum supported server</span></span><br/> | <span data-ttu-id="55ed5-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55ed5-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55ed5-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="55ed5-166">Namespace</span></span><br/>                | <span data-ttu-id="55ed5-167">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55ed5-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55ed5-168">MOF</span><span class="sxs-lookup"><span data-stu-id="55ed5-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55ed5-169"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55ed5-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55ed5-170">DLL</span><span class="sxs-lookup"><span data-stu-id="55ed5-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55ed5-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55ed5-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ed5-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55ed5-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ed5-173">CIM \_ 資料檔案</span><span class="sxs-lookup"><span data-stu-id="55ed5-173">CIM\_DataFile</span></span>](takeownershipex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="55ed5-174">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="55ed5-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="55ed5-175">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="55ed5-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="55ed5-176">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="55ed5-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

