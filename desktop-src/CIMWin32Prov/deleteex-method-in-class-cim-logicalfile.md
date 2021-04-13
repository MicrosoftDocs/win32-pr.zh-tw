---
description: DeleteEx 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。 這個方法是刪除方法的擴充版本。
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510511"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="7e989-104">CIM LogicalFile 類別的 DeleteEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7e989-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="7e989-105">**DeleteEx** 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="7e989-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="7e989-106">這個方法是 [**刪除**](delete-method-in-class-cim-logicalfile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="7e989-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e989-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7e989-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7e989-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7e989-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7e989-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="7e989-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7e989-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="7e989-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e989-111">語法</span><span class="sxs-lookup"><span data-stu-id="7e989-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="7e989-112">參數</span><span class="sxs-lookup"><span data-stu-id="7e989-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e989-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7e989-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e989-114">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7e989-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="7e989-115">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="7e989-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-116">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7e989-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7e989-117">將子檔案命名為 (或目錄) 的字串，做為方法的起點。</span><span class="sxs-lookup"><span data-stu-id="7e989-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="7e989-118">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="7e989-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="7e989-119">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="7e989-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e989-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e989-120">Return value</span></span>

<span data-ttu-id="7e989-121">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="7e989-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7e989-122">「成功」</span><span class="sxs-lookup"><span data-stu-id="7e989-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-123">0</span><span class="sxs-lookup"><span data-stu-id="7e989-123">0</span></span>

<span data-ttu-id="7e989-124">成功。</span><span class="sxs-lookup"><span data-stu-id="7e989-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-125">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="7e989-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-126">2</span><span class="sxs-lookup"><span data-stu-id="7e989-126">2</span></span>

<span data-ttu-id="7e989-127">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="7e989-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-128">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="7e989-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-129">8</span><span class="sxs-lookup"><span data-stu-id="7e989-129">8</span></span>

<span data-ttu-id="7e989-130">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="7e989-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-131">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="7e989-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-132">9</span><span class="sxs-lookup"><span data-stu-id="7e989-132">9</span></span>

<span data-ttu-id="7e989-133">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="7e989-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-134">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="7e989-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-135">10</span><span class="sxs-lookup"><span data-stu-id="7e989-135">10</span></span>

<span data-ttu-id="7e989-136">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="7e989-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-137">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="7e989-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-138">11</span><span class="sxs-lookup"><span data-stu-id="7e989-138">11</span></span>

<span data-ttu-id="7e989-139">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="7e989-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-140">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="7e989-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-141">12</span><span class="sxs-lookup"><span data-stu-id="7e989-141">12</span></span>

<span data-ttu-id="7e989-142">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="7e989-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-143">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="7e989-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-144">13</span><span class="sxs-lookup"><span data-stu-id="7e989-144">13</span></span>

<span data-ttu-id="7e989-145">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="7e989-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-146">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="7e989-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-147">14</span><span class="sxs-lookup"><span data-stu-id="7e989-147">14</span></span>

<span data-ttu-id="7e989-148">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="7e989-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-149">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="7e989-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-150">15</span><span class="sxs-lookup"><span data-stu-id="7e989-150">15</span></span>

<span data-ttu-id="7e989-151">共用違規。</span><span class="sxs-lookup"><span data-stu-id="7e989-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-152">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="7e989-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-153">16</span><span class="sxs-lookup"><span data-stu-id="7e989-153">16</span></span>

<span data-ttu-id="7e989-154">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="7e989-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-155">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="7e989-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-156">17</span><span class="sxs-lookup"><span data-stu-id="7e989-156">17</span></span>

<span data-ttu-id="7e989-157">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="7e989-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="7e989-158">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="7e989-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7e989-159">21</span><span class="sxs-lookup"><span data-stu-id="7e989-159">21</span></span>

<span data-ttu-id="7e989-160">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="7e989-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e989-161">備註</span><span class="sxs-lookup"><span data-stu-id="7e989-161">Remarks</span></span>

<span data-ttu-id="7e989-162">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="7e989-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7e989-163">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="7e989-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7e989-164">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7e989-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7e989-165">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7e989-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e989-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e989-166">Requirements</span></span>



| <span data-ttu-id="7e989-167">需求</span><span class="sxs-lookup"><span data-stu-id="7e989-167">Requirement</span></span> | <span data-ttu-id="7e989-168">值</span><span class="sxs-lookup"><span data-stu-id="7e989-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e989-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e989-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7e989-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e989-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e989-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e989-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7e989-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e989-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e989-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="7e989-173">Namespace</span></span><br/>                | <span data-ttu-id="7e989-174">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e989-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e989-175">MOF</span><span class="sxs-lookup"><span data-stu-id="7e989-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e989-176"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e989-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e989-177">DLL</span><span class="sxs-lookup"><span data-stu-id="7e989-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e989-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e989-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e989-179">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e989-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e989-180">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="7e989-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="7e989-181">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="7e989-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

