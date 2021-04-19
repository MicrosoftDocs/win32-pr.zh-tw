---
description: 取得物件路徑中指定之邏輯檔案的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本。
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973152"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="a842d-104">CIM LogicalFile 類別的 TakeOwnerShipEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a842d-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="a842d-105">**TakeOwnerShipEx** 方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="a842d-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="a842d-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="a842d-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="a842d-107">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="a842d-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a842d-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a842d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a842d-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a842d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a842d-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a842d-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a842d-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a842d-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a842d-112">語法</span><span class="sxs-lookup"><span data-stu-id="a842d-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="a842d-113">參數</span><span class="sxs-lookup"><span data-stu-id="a842d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a842d-114">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a842d-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a842d-115">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a842d-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="a842d-116">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="a842d-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-117">*StartFileName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a842d-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a842d-118">將子檔案命名為 (或目錄) 的字串，做為方法的起點。</span><span class="sxs-lookup"><span data-stu-id="a842d-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="a842d-119">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="a842d-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="a842d-120">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="a842d-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-121">*遞迴* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a842d-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a842d-122">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ LogicalFile**](cim-logicalfile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="a842d-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="a842d-123">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="a842d-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a842d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="a842d-124">Return value</span></span>

<span data-ttu-id="a842d-125">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a842d-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a842d-126">「成功」</span><span class="sxs-lookup"><span data-stu-id="a842d-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-127">0</span><span class="sxs-lookup"><span data-stu-id="a842d-127">0</span></span>

<span data-ttu-id="a842d-128">成功。</span><span class="sxs-lookup"><span data-stu-id="a842d-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-129">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="a842d-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-130">2</span><span class="sxs-lookup"><span data-stu-id="a842d-130">2</span></span>

<span data-ttu-id="a842d-131">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a842d-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-132">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="a842d-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-133">8</span><span class="sxs-lookup"><span data-stu-id="a842d-133">8</span></span>

<span data-ttu-id="a842d-134">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="a842d-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-135">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="a842d-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-136">9</span><span class="sxs-lookup"><span data-stu-id="a842d-136">9</span></span>

<span data-ttu-id="a842d-137">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="a842d-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-138">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="a842d-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-139">10</span><span class="sxs-lookup"><span data-stu-id="a842d-139">10</span></span>

<span data-ttu-id="a842d-140">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="a842d-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-141">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="a842d-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-142">11</span><span class="sxs-lookup"><span data-stu-id="a842d-142">11</span></span>

<span data-ttu-id="a842d-143">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="a842d-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-144">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="a842d-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-145">12</span><span class="sxs-lookup"><span data-stu-id="a842d-145">12</span></span>

<span data-ttu-id="a842d-146">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="a842d-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-147">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="a842d-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-148">13</span><span class="sxs-lookup"><span data-stu-id="a842d-148">13</span></span>

<span data-ttu-id="a842d-149">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="a842d-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-150">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="a842d-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-151">14</span><span class="sxs-lookup"><span data-stu-id="a842d-151">14</span></span>

<span data-ttu-id="a842d-152">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="a842d-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-153">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="a842d-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-154">15</span><span class="sxs-lookup"><span data-stu-id="a842d-154">15</span></span>

<span data-ttu-id="a842d-155">共用違規。</span><span class="sxs-lookup"><span data-stu-id="a842d-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-156">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="a842d-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-157">16</span><span class="sxs-lookup"><span data-stu-id="a842d-157">16</span></span>

<span data-ttu-id="a842d-158">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="a842d-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-159">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="a842d-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-160">17</span><span class="sxs-lookup"><span data-stu-id="a842d-160">17</span></span>

<span data-ttu-id="a842d-161">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="a842d-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a842d-162">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="a842d-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a842d-163">21</span><span class="sxs-lookup"><span data-stu-id="a842d-163">21</span></span>

<span data-ttu-id="a842d-164">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="a842d-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a842d-165">備註</span><span class="sxs-lookup"><span data-stu-id="a842d-165">Remarks</span></span>

<span data-ttu-id="a842d-166">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a842d-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a842d-167">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a842d-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a842d-168">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a842d-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a842d-169">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a842d-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a842d-170">規格需求</span><span class="sxs-lookup"><span data-stu-id="a842d-170">Requirements</span></span>



| <span data-ttu-id="a842d-171">需求</span><span class="sxs-lookup"><span data-stu-id="a842d-171">Requirement</span></span> | <span data-ttu-id="a842d-172">值</span><span class="sxs-lookup"><span data-stu-id="a842d-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a842d-173">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a842d-173">Minimum supported client</span></span><br/> | <span data-ttu-id="a842d-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a842d-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a842d-175">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a842d-175">Minimum supported server</span></span><br/> | <span data-ttu-id="a842d-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a842d-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a842d-177">命名空間</span><span class="sxs-lookup"><span data-stu-id="a842d-177">Namespace</span></span><br/>                | <span data-ttu-id="a842d-178">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a842d-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a842d-179">MOF</span><span class="sxs-lookup"><span data-stu-id="a842d-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a842d-180"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a842d-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a842d-181">DLL</span><span class="sxs-lookup"><span data-stu-id="a842d-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a842d-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a842d-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a842d-183">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a842d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a842d-184">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="a842d-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="a842d-185">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="a842d-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

