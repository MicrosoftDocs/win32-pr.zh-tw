---
description: CopyEx 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到 FileName 參數所指定的位置。
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: CIM_DataFile 類別的 CopyEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973582"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="8e03b-103">CIM \_ 資料檔案類別的 CopyEx 方法</span><span class="sxs-lookup"><span data-stu-id="8e03b-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="8e03b-104">**CopyEx** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="8e03b-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="8e03b-105">如果需要覆寫現有的邏輯檔案，則不支援複本。</span><span class="sxs-lookup"><span data-stu-id="8e03b-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="8e03b-106">這個方法是 [**複製**](copy-method-in-class-cim-datafile.md) 方法的擴充版本，並且繼承自 [CIM \_ LogicalFile](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="8e03b-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e03b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="8e03b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e03b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="8e03b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e03b-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8e03b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e03b-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8e03b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e03b-111">語法</span><span class="sxs-lookup"><span data-stu-id="8e03b-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8e03b-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e03b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e03b-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e03b-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e03b-114">目的地檔 (或目錄) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="8e03b-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="8e03b-115">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="8e03b-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="8e03b-116">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8e03b-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e03b-117">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e03b-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8e03b-118">如果方法成功，此參數將會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="8e03b-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8e03b-119">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e03b-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e03b-120">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="8e03b-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8e03b-121">一般而言， *StartFileName* 參數是 *StopFileName* 參數，可指定上一個方法呼叫發生錯誤 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="8e03b-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8e03b-122">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="8e03b-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="8e03b-123">如果使用 *StartFileName* ，則 *遞迴* 也必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="8e03b-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="8e03b-124">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e03b-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e03b-125">若為 TRUE，則此方法也會以遞迴方式套用至 [**CIM \_ 資料檔案**](cim-datafile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="8e03b-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="8e03b-126">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="8e03b-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e03b-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e03b-127">Return value</span></span>

<span data-ttu-id="8e03b-128">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e03b-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="8e03b-129">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="8e03b-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8e03b-130">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="8e03b-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-131">0</span><span class="sxs-lookup"><span data-stu-id="8e03b-131">0</span></span>

<span data-ttu-id="8e03b-132">成功。</span><span class="sxs-lookup"><span data-stu-id="8e03b-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-133">2</span><span class="sxs-lookup"><span data-stu-id="8e03b-133">2</span></span>

<span data-ttu-id="8e03b-134">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8e03b-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-135">8</span><span class="sxs-lookup"><span data-stu-id="8e03b-135">8</span></span>

<span data-ttu-id="8e03b-136">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="8e03b-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-137">9</span><span class="sxs-lookup"><span data-stu-id="8e03b-137">9</span></span>

<span data-ttu-id="8e03b-138">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="8e03b-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-139">10</span><span class="sxs-lookup"><span data-stu-id="8e03b-139">10</span></span>

<span data-ttu-id="8e03b-140">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="8e03b-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-141">11</span><span class="sxs-lookup"><span data-stu-id="8e03b-141">11</span></span>

<span data-ttu-id="8e03b-142">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="8e03b-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-143">12</span><span class="sxs-lookup"><span data-stu-id="8e03b-143">12</span></span>

<span data-ttu-id="8e03b-144">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="8e03b-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-145">13</span><span class="sxs-lookup"><span data-stu-id="8e03b-145">13</span></span>

<span data-ttu-id="8e03b-146">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="8e03b-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-147">14</span><span class="sxs-lookup"><span data-stu-id="8e03b-147">14</span></span>

<span data-ttu-id="8e03b-148">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="8e03b-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-149">15</span><span class="sxs-lookup"><span data-stu-id="8e03b-149">15</span></span>

<span data-ttu-id="8e03b-150">共用違規。</span><span class="sxs-lookup"><span data-stu-id="8e03b-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-151">16</span><span class="sxs-lookup"><span data-stu-id="8e03b-151">16</span></span>

<span data-ttu-id="8e03b-152">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="8e03b-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-153">17</span><span class="sxs-lookup"><span data-stu-id="8e03b-153">17</span></span>

<span data-ttu-id="8e03b-154">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="8e03b-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8e03b-155">21</span><span class="sxs-lookup"><span data-stu-id="8e03b-155">21</span></span>

<span data-ttu-id="8e03b-156">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="8e03b-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e03b-157">備註</span><span class="sxs-lookup"><span data-stu-id="8e03b-157">Remarks</span></span>

<span data-ttu-id="8e03b-158">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **COPYEX** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="8e03b-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="8e03b-159">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="8e03b-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e03b-160">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8e03b-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e03b-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e03b-161">Requirements</span></span>



| <span data-ttu-id="8e03b-162">需求</span><span class="sxs-lookup"><span data-stu-id="8e03b-162">Requirement</span></span> | <span data-ttu-id="8e03b-163">值</span><span class="sxs-lookup"><span data-stu-id="8e03b-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e03b-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e03b-164">Minimum supported client</span></span><br/> | <span data-ttu-id="8e03b-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e03b-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e03b-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e03b-166">Minimum supported server</span></span><br/> | <span data-ttu-id="8e03b-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e03b-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e03b-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="8e03b-168">Namespace</span></span><br/>                | <span data-ttu-id="8e03b-169">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e03b-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e03b-170">MOF</span><span class="sxs-lookup"><span data-stu-id="8e03b-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e03b-171"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e03b-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e03b-172">DLL</span><span class="sxs-lookup"><span data-stu-id="8e03b-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e03b-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e03b-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e03b-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e03b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e03b-175">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="8e03b-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="8e03b-176">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="8e03b-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="8e03b-177">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="8e03b-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

