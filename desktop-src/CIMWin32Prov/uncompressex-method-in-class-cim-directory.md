---
description: Uncompresses 邏輯目錄專案檔 (或在物件路徑中指定的目錄) 。 這個方法是解壓縮方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: ef5b7c90-5013-4ec0-bfa6-c32428ffb501
ms.tgt_platform: multiple
title: CIM_Directory 類別的 UncompressEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af74132ceeb67e48d39c22bd0172954f26707f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510692"
---
# <a name="uncompressex-method-of-the-cim_directory-class"></a><span data-ttu-id="997d3-104">CIM 目錄類別的 UncompressEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="997d3-104">UncompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="997d3-105">**UncompressEx** 方法會 uncompresses 邏輯目錄專案檔， (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="997d3-105">The **UncompressEx** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="997d3-106">這個方法是 [**解壓縮**](uncompress-method-in-class-cim-directory.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="997d3-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="997d3-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="997d3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="997d3-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="997d3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="997d3-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="997d3-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="997d3-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="997d3-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="997d3-111">語法</span><span class="sxs-lookup"><span data-stu-id="997d3-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="997d3-112">參數</span><span class="sxs-lookup"><span data-stu-id="997d3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="997d3-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="997d3-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="997d3-114">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="997d3-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="997d3-115">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="997d3-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="997d3-116">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="997d3-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997d3-117">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="997d3-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="997d3-118">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="997d3-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="997d3-119">如果這個參數是 **null**，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="997d3-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="997d3-120">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="997d3-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997d3-121">若 **為 TRUE**，則會以遞迴方式將方法套用至 [**CIM \_ 目錄**](cim-directory.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="997d3-121">If **TRUE**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="997d3-122">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="997d3-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="997d3-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="997d3-123">Return value</span></span>

<span data-ttu-id="997d3-124">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="997d3-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="997d3-125">0</span><span class="sxs-lookup"><span data-stu-id="997d3-125">0</span></span>

<span data-ttu-id="997d3-126">成功。</span><span class="sxs-lookup"><span data-stu-id="997d3-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-127">2</span><span class="sxs-lookup"><span data-stu-id="997d3-127">2</span></span>

<span data-ttu-id="997d3-128">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="997d3-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-129">8</span><span class="sxs-lookup"><span data-stu-id="997d3-129">8</span></span>

<span data-ttu-id="997d3-130">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="997d3-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-131">9</span><span class="sxs-lookup"><span data-stu-id="997d3-131">9</span></span>

<span data-ttu-id="997d3-132">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="997d3-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-133">10</span><span class="sxs-lookup"><span data-stu-id="997d3-133">10</span></span>

<span data-ttu-id="997d3-134">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="997d3-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-135">11</span><span class="sxs-lookup"><span data-stu-id="997d3-135">11</span></span>

<span data-ttu-id="997d3-136">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="997d3-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-137">12</span><span class="sxs-lookup"><span data-stu-id="997d3-137">12</span></span>

<span data-ttu-id="997d3-138">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="997d3-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-139">13</span><span class="sxs-lookup"><span data-stu-id="997d3-139">13</span></span>

<span data-ttu-id="997d3-140">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="997d3-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-141">14</span><span class="sxs-lookup"><span data-stu-id="997d3-141">14</span></span>

<span data-ttu-id="997d3-142">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="997d3-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-143">15</span><span class="sxs-lookup"><span data-stu-id="997d3-143">15</span></span>

<span data-ttu-id="997d3-144">共用違規。</span><span class="sxs-lookup"><span data-stu-id="997d3-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-145">16</span><span class="sxs-lookup"><span data-stu-id="997d3-145">16</span></span>

<span data-ttu-id="997d3-146">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="997d3-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-147">17</span><span class="sxs-lookup"><span data-stu-id="997d3-147">17</span></span>

<span data-ttu-id="997d3-148">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="997d3-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="997d3-149">21</span><span class="sxs-lookup"><span data-stu-id="997d3-149">21</span></span>

<span data-ttu-id="997d3-150">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="997d3-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="997d3-151">備註</span><span class="sxs-lookup"><span data-stu-id="997d3-151">Remarks</span></span>

<span data-ttu-id="997d3-152">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="997d3-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="997d3-153">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="997d3-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="997d3-154">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="997d3-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="997d3-155">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="997d3-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="997d3-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="997d3-156">Requirements</span></span>



| <span data-ttu-id="997d3-157">需求</span><span class="sxs-lookup"><span data-stu-id="997d3-157">Requirement</span></span> | <span data-ttu-id="997d3-158">值</span><span class="sxs-lookup"><span data-stu-id="997d3-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="997d3-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="997d3-159">Minimum supported client</span></span><br/> | <span data-ttu-id="997d3-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="997d3-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="997d3-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="997d3-161">Minimum supported server</span></span><br/> | <span data-ttu-id="997d3-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="997d3-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="997d3-163">命名空間</span><span class="sxs-lookup"><span data-stu-id="997d3-163">Namespace</span></span><br/>                | <span data-ttu-id="997d3-164">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="997d3-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="997d3-165">MOF</span><span class="sxs-lookup"><span data-stu-id="997d3-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="997d3-166"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="997d3-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="997d3-167">DLL</span><span class="sxs-lookup"><span data-stu-id="997d3-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="997d3-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="997d3-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997d3-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="997d3-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997d3-170">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="997d3-170">**CIM\_Directory**</span></span>](uncompressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="997d3-171">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="997d3-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

