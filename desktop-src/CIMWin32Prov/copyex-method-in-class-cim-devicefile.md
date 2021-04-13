---
description: 將物件路徑中指定的邏輯裝置檔案 (或目錄) 複製到 FileName 參數所指定的位置。
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 CopyEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385943"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="81a0e-103">CIM DeviceFile 類別的 CopyEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="81a0e-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="81a0e-104">**CopyEx** 方法會將物件路徑中指定的邏輯裝置檔案 (或目錄) 複製到 *FileName* 參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="81a0e-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="81a0e-105">如果需要覆寫現有的邏輯檔案，則不支援複製。</span><span class="sxs-lookup"><span data-stu-id="81a0e-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="81a0e-106">這個方法是 [**複製**](copy-method-in-class-cim-devicefile.md) 方法的擴充版本。</span><span class="sxs-lookup"><span data-stu-id="81a0e-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="81a0e-107">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="81a0e-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81a0e-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="81a0e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81a0e-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="81a0e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81a0e-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="81a0e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81a0e-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="81a0e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81a0e-112">語法</span><span class="sxs-lookup"><span data-stu-id="81a0e-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="81a0e-113">參數</span><span class="sxs-lookup"><span data-stu-id="81a0e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a0e-114">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81a0e-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a0e-115">目的地檔 (或目錄) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="81a0e-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="81a0e-116">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="81a0e-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="81a0e-117">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81a0e-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81a0e-118">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="81a0e-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="81a0e-119">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="81a0e-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="81a0e-120">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81a0e-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a0e-121">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="81a0e-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="81a0e-122">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="81a0e-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="81a0e-123">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="81a0e-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="81a0e-124">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81a0e-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a0e-125">若為 TRUE，則此方法也會以遞迴方式套用至 [**CIM \_ DeviceFile**](cim-devicefile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="81a0e-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="81a0e-126">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="81a0e-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a0e-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="81a0e-127">Return value</span></span>

<span data-ttu-id="81a0e-128">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="81a0e-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-129">0</span><span class="sxs-lookup"><span data-stu-id="81a0e-129">0</span></span>

<span data-ttu-id="81a0e-130">成功。</span><span class="sxs-lookup"><span data-stu-id="81a0e-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-131">2</span><span class="sxs-lookup"><span data-stu-id="81a0e-131">2</span></span>

<span data-ttu-id="81a0e-132">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="81a0e-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-133">8</span><span class="sxs-lookup"><span data-stu-id="81a0e-133">8</span></span>

<span data-ttu-id="81a0e-134">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="81a0e-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-135">9</span><span class="sxs-lookup"><span data-stu-id="81a0e-135">9</span></span>

<span data-ttu-id="81a0e-136">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="81a0e-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-137">10</span><span class="sxs-lookup"><span data-stu-id="81a0e-137">10</span></span>

<span data-ttu-id="81a0e-138">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="81a0e-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-139">11</span><span class="sxs-lookup"><span data-stu-id="81a0e-139">11</span></span>

<span data-ttu-id="81a0e-140">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="81a0e-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-141">12</span><span class="sxs-lookup"><span data-stu-id="81a0e-141">12</span></span>

<span data-ttu-id="81a0e-142">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="81a0e-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-143">13</span><span class="sxs-lookup"><span data-stu-id="81a0e-143">13</span></span>

<span data-ttu-id="81a0e-144">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="81a0e-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-145">14</span><span class="sxs-lookup"><span data-stu-id="81a0e-145">14</span></span>

<span data-ttu-id="81a0e-146">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="81a0e-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-147">15</span><span class="sxs-lookup"><span data-stu-id="81a0e-147">15</span></span>

<span data-ttu-id="81a0e-148">共用違規。</span><span class="sxs-lookup"><span data-stu-id="81a0e-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-149">16</span><span class="sxs-lookup"><span data-stu-id="81a0e-149">16</span></span>

<span data-ttu-id="81a0e-150">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="81a0e-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-151">17</span><span class="sxs-lookup"><span data-stu-id="81a0e-151">17</span></span>

<span data-ttu-id="81a0e-152">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="81a0e-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="81a0e-153">21</span><span class="sxs-lookup"><span data-stu-id="81a0e-153">21</span></span>

<span data-ttu-id="81a0e-154">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="81a0e-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81a0e-155">備註</span><span class="sxs-lookup"><span data-stu-id="81a0e-155">Remarks</span></span>

<span data-ttu-id="81a0e-156">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="81a0e-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="81a0e-157">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="81a0e-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="81a0e-158">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="81a0e-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81a0e-159">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="81a0e-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a0e-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="81a0e-160">Requirements</span></span>



| <span data-ttu-id="81a0e-161">需求</span><span class="sxs-lookup"><span data-stu-id="81a0e-161">Requirement</span></span> | <span data-ttu-id="81a0e-162">值</span><span class="sxs-lookup"><span data-stu-id="81a0e-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81a0e-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81a0e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="81a0e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81a0e-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81a0e-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81a0e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="81a0e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81a0e-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81a0e-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="81a0e-167">Namespace</span></span><br/>                | <span data-ttu-id="81a0e-168">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81a0e-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81a0e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="81a0e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81a0e-170"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="81a0e-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81a0e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="81a0e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a0e-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a0e-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a0e-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81a0e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a0e-174">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="81a0e-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="81a0e-175">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="81a0e-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

