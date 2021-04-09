---
description: DeleteEx 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。 這個方法是 Delete 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110521"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="461e7-104">CIM \_ 資料檔案類別的 DeleteEx 方法</span><span class="sxs-lookup"><span data-stu-id="461e7-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="461e7-105">**DeleteEx** 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="461e7-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="461e7-106">這個方法是 [**Delete**](delete-method-in-class-cim-datafile.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="461e7-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="461e7-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="461e7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="461e7-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="461e7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="461e7-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="461e7-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="461e7-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="461e7-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="461e7-111">語法</span><span class="sxs-lookup"><span data-stu-id="461e7-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="461e7-112">參數</span><span class="sxs-lookup"><span data-stu-id="461e7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461e7-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="461e7-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="461e7-114">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="461e7-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="461e7-115">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="461e7-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="461e7-116">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="461e7-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="461e7-117">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="461e7-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="461e7-118">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="461e7-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="461e7-119">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="461e7-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461e7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="461e7-120">Return value</span></span>

<span data-ttu-id="461e7-121">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="461e7-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="461e7-122">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="461e7-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="461e7-123">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="461e7-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="461e7-124">0</span><span class="sxs-lookup"><span data-stu-id="461e7-124">0</span></span>

<span data-ttu-id="461e7-125">成功。</span><span class="sxs-lookup"><span data-stu-id="461e7-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-126">2</span><span class="sxs-lookup"><span data-stu-id="461e7-126">2</span></span>

<span data-ttu-id="461e7-127">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="461e7-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-128">8</span><span class="sxs-lookup"><span data-stu-id="461e7-128">8</span></span>

<span data-ttu-id="461e7-129">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="461e7-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-130">9</span><span class="sxs-lookup"><span data-stu-id="461e7-130">9</span></span>

<span data-ttu-id="461e7-131">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="461e7-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-132">10</span><span class="sxs-lookup"><span data-stu-id="461e7-132">10</span></span>

<span data-ttu-id="461e7-133">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="461e7-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-134">11</span><span class="sxs-lookup"><span data-stu-id="461e7-134">11</span></span>

<span data-ttu-id="461e7-135">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="461e7-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-136">12</span><span class="sxs-lookup"><span data-stu-id="461e7-136">12</span></span>

<span data-ttu-id="461e7-137">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="461e7-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-138">13</span><span class="sxs-lookup"><span data-stu-id="461e7-138">13</span></span>

<span data-ttu-id="461e7-139">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="461e7-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-140">14</span><span class="sxs-lookup"><span data-stu-id="461e7-140">14</span></span>

<span data-ttu-id="461e7-141">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="461e7-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-142">15</span><span class="sxs-lookup"><span data-stu-id="461e7-142">15</span></span>

<span data-ttu-id="461e7-143">共用違規。</span><span class="sxs-lookup"><span data-stu-id="461e7-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-144">16</span><span class="sxs-lookup"><span data-stu-id="461e7-144">16</span></span>

<span data-ttu-id="461e7-145">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="461e7-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-146">17</span><span class="sxs-lookup"><span data-stu-id="461e7-146">17</span></span>

<span data-ttu-id="461e7-147">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="461e7-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="461e7-148">21</span><span class="sxs-lookup"><span data-stu-id="461e7-148">21</span></span>

<span data-ttu-id="461e7-149">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="461e7-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="461e7-150">備註</span><span class="sxs-lookup"><span data-stu-id="461e7-150">Remarks</span></span>

<span data-ttu-id="461e7-151">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **DELETEEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="461e7-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="461e7-152">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="461e7-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="461e7-153">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="461e7-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="461e7-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="461e7-154">Requirements</span></span>



| <span data-ttu-id="461e7-155">需求</span><span class="sxs-lookup"><span data-stu-id="461e7-155">Requirement</span></span> | <span data-ttu-id="461e7-156">值</span><span class="sxs-lookup"><span data-stu-id="461e7-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="461e7-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="461e7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="461e7-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="461e7-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="461e7-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="461e7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="461e7-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="461e7-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="461e7-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="461e7-161">Namespace</span></span><br/>                | <span data-ttu-id="461e7-162">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="461e7-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="461e7-163">MOF</span><span class="sxs-lookup"><span data-stu-id="461e7-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="461e7-164"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="461e7-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="461e7-165">DLL</span><span class="sxs-lookup"><span data-stu-id="461e7-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="461e7-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="461e7-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="461e7-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="461e7-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="461e7-168">CIM \_ 資料檔案</span><span class="sxs-lookup"><span data-stu-id="461e7-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="461e7-169">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="461e7-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="461e7-170">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="461e7-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="461e7-171">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="461e7-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

