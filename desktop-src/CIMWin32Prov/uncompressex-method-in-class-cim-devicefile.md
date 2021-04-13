---
description: Uncompresses 邏輯裝置檔案 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510693"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="db53b-105">CIM DeviceFile 類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="db53b-105">UncompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="db53b-106">**UncompressEx** 方法會 uncompresses 邏輯裝置檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="db53b-106">The **UncompressEx** method uncompresses the logical device file (or directory) specified in the object path.</span></span> <span data-ttu-id="db53b-107">這個方法是 [**解壓縮**](uncompress-method-in-class-cim-devicefile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="db53b-107">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="db53b-108">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="db53b-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db53b-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="db53b-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="db53b-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="db53b-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="db53b-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="db53b-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db53b-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="db53b-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db53b-113">語法</span><span class="sxs-lookup"><span data-stu-id="db53b-113">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="db53b-114">參數</span><span class="sxs-lookup"><span data-stu-id="db53b-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db53b-115">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="db53b-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db53b-116">表示方法失敗 (或目錄) 之檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="db53b-116">String that represent the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="db53b-117">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="db53b-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="db53b-118">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db53b-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db53b-119">字串，表示要作為方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="db53b-119">String that represents the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="db53b-120">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="db53b-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="db53b-121">如果這個參數是 **Null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="db53b-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="db53b-122">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db53b-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db53b-123">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ DeviceFile**](cim-devicefile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="db53b-123">If **TRUE**, this method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="db53b-124">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="db53b-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db53b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="db53b-125">Return value</span></span>

<span data-ttu-id="db53b-126">在成功時傳回0的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="db53b-126">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="db53b-127">0</span><span class="sxs-lookup"><span data-stu-id="db53b-127">0</span></span>

<span data-ttu-id="db53b-128">成功。</span><span class="sxs-lookup"><span data-stu-id="db53b-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-129">2</span><span class="sxs-lookup"><span data-stu-id="db53b-129">2</span></span>

<span data-ttu-id="db53b-130">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="db53b-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-131">8</span><span class="sxs-lookup"><span data-stu-id="db53b-131">8</span></span>

<span data-ttu-id="db53b-132">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="db53b-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-133">9</span><span class="sxs-lookup"><span data-stu-id="db53b-133">9</span></span>

<span data-ttu-id="db53b-134">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="db53b-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-135">10</span><span class="sxs-lookup"><span data-stu-id="db53b-135">10</span></span>

<span data-ttu-id="db53b-136">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="db53b-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-137">11</span><span class="sxs-lookup"><span data-stu-id="db53b-137">11</span></span>

<span data-ttu-id="db53b-138">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="db53b-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-139">12</span><span class="sxs-lookup"><span data-stu-id="db53b-139">12</span></span>

<span data-ttu-id="db53b-140">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="db53b-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-141">13</span><span class="sxs-lookup"><span data-stu-id="db53b-141">13</span></span>

<span data-ttu-id="db53b-142">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="db53b-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-143">14</span><span class="sxs-lookup"><span data-stu-id="db53b-143">14</span></span>

<span data-ttu-id="db53b-144">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="db53b-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-145">15</span><span class="sxs-lookup"><span data-stu-id="db53b-145">15</span></span>

<span data-ttu-id="db53b-146">共用違規。</span><span class="sxs-lookup"><span data-stu-id="db53b-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-147">16</span><span class="sxs-lookup"><span data-stu-id="db53b-147">16</span></span>

<span data-ttu-id="db53b-148">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="db53b-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-149">17</span><span class="sxs-lookup"><span data-stu-id="db53b-149">17</span></span>

<span data-ttu-id="db53b-150">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="db53b-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="db53b-151">21</span><span class="sxs-lookup"><span data-stu-id="db53b-151">21</span></span>

<span data-ttu-id="db53b-152">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="db53b-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db53b-153">備註</span><span class="sxs-lookup"><span data-stu-id="db53b-153">Remarks</span></span>

<span data-ttu-id="db53b-154">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="db53b-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="db53b-155">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="db53b-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="db53b-156">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="db53b-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="db53b-157">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="db53b-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="db53b-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="db53b-158">Requirements</span></span>



| <span data-ttu-id="db53b-159">需求</span><span class="sxs-lookup"><span data-stu-id="db53b-159">Requirement</span></span> | <span data-ttu-id="db53b-160">值</span><span class="sxs-lookup"><span data-stu-id="db53b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db53b-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db53b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="db53b-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db53b-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db53b-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db53b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="db53b-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db53b-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db53b-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="db53b-165">Namespace</span></span><br/>                | <span data-ttu-id="db53b-166">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db53b-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db53b-167">MOF</span><span class="sxs-lookup"><span data-stu-id="db53b-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db53b-168"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="db53b-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db53b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="db53b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db53b-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db53b-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db53b-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db53b-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db53b-172">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="db53b-172">CIM\_DeviceFile</span></span>](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="db53b-173">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="db53b-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

