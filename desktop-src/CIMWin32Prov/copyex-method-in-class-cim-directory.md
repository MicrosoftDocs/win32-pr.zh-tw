---
description: CopyEx 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到 FileName 參數所指定的位置。 這個方法是複製方法的擴充版本，並且繼承自 CIM \_ LogicalFile。
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: CIM_Directory 類別的 CopyEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936144"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="53879-104">CIM 目錄類別的 CopyEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="53879-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="53879-105">**CopyEx** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="53879-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="53879-106">這個方法是 [**複製**](copy-method-in-class-cim-directory.md) 方法的擴充版本，並且繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="53879-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="53879-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="53879-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="53879-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="53879-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="53879-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="53879-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="53879-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="53879-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="53879-111">語法</span><span class="sxs-lookup"><span data-stu-id="53879-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="53879-112">參數</span><span class="sxs-lookup"><span data-stu-id="53879-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53879-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53879-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53879-114">目的地檔 (或目錄) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="53879-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="53879-115">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="53879-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="53879-116">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="53879-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53879-117">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="53879-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="53879-118">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="53879-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="53879-119">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53879-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53879-120">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="53879-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="53879-121">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="53879-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="53879-122">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="53879-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="53879-123">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="53879-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53879-124">若為 TRUE，則此方法也會以遞迴方式套用至 [**CIM \_ 目錄**](cim-directory.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="53879-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="53879-125">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="53879-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53879-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="53879-126">Return value</span></span>

<span data-ttu-id="53879-127">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="53879-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="53879-128">0</span><span class="sxs-lookup"><span data-stu-id="53879-128">0</span></span>

<span data-ttu-id="53879-129">成功。</span><span class="sxs-lookup"><span data-stu-id="53879-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-130">2</span><span class="sxs-lookup"><span data-stu-id="53879-130">2</span></span>

<span data-ttu-id="53879-131">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="53879-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-132">8</span><span class="sxs-lookup"><span data-stu-id="53879-132">8</span></span>

<span data-ttu-id="53879-133">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="53879-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-134">9</span><span class="sxs-lookup"><span data-stu-id="53879-134">9</span></span>

<span data-ttu-id="53879-135">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="53879-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-136">10</span><span class="sxs-lookup"><span data-stu-id="53879-136">10</span></span>

<span data-ttu-id="53879-137">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="53879-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-138">11</span><span class="sxs-lookup"><span data-stu-id="53879-138">11</span></span>

<span data-ttu-id="53879-139">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="53879-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-140">12</span><span class="sxs-lookup"><span data-stu-id="53879-140">12</span></span>

<span data-ttu-id="53879-141">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="53879-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-142">13</span><span class="sxs-lookup"><span data-stu-id="53879-142">13</span></span>

<span data-ttu-id="53879-143">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="53879-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-144">14</span><span class="sxs-lookup"><span data-stu-id="53879-144">14</span></span>

<span data-ttu-id="53879-145">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="53879-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-146">15</span><span class="sxs-lookup"><span data-stu-id="53879-146">15</span></span>

<span data-ttu-id="53879-147">共用違規。</span><span class="sxs-lookup"><span data-stu-id="53879-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-148">16</span><span class="sxs-lookup"><span data-stu-id="53879-148">16</span></span>

<span data-ttu-id="53879-149">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="53879-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-150">17</span><span class="sxs-lookup"><span data-stu-id="53879-150">17</span></span>

<span data-ttu-id="53879-151">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="53879-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="53879-152">21</span><span class="sxs-lookup"><span data-stu-id="53879-152">21</span></span>

<span data-ttu-id="53879-153">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="53879-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53879-154">備註</span><span class="sxs-lookup"><span data-stu-id="53879-154">Remarks</span></span>

<span data-ttu-id="53879-155">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="53879-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="53879-156">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="53879-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="53879-157">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="53879-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="53879-158">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="53879-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53879-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="53879-159">Requirements</span></span>



| <span data-ttu-id="53879-160">需求</span><span class="sxs-lookup"><span data-stu-id="53879-160">Requirement</span></span> | <span data-ttu-id="53879-161">值</span><span class="sxs-lookup"><span data-stu-id="53879-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53879-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53879-162">Minimum supported client</span></span><br/> | <span data-ttu-id="53879-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53879-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53879-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53879-164">Minimum supported server</span></span><br/> | <span data-ttu-id="53879-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53879-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53879-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="53879-166">Namespace</span></span><br/>                | <span data-ttu-id="53879-167">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="53879-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="53879-168">MOF</span><span class="sxs-lookup"><span data-stu-id="53879-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53879-169"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="53879-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="53879-170">DLL</span><span class="sxs-lookup"><span data-stu-id="53879-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53879-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53879-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53879-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53879-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53879-173">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="53879-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="53879-174">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="53879-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

