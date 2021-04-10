---
description: 重新命名方法會重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。
ms.assetid: 3eaf9f4f-270e-41d0-86ae-c5edb1850ef5
ms.tgt_platform: multiple
title: CIM_DataFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aea061990a6d3bd52a98dc9101102059767ecf9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111260"
---
# <a name="rename-method-of-the-cim_datafile-class"></a><span data-ttu-id="5628c-103">CIM 資料檔案類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="5628c-103">Rename method of the CIM\_DataFile class</span></span>

<span data-ttu-id="5628c-104">**重新命名** 方法會重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="5628c-104">The **Rename** method renames the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="5628c-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="5628c-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span> <span data-ttu-id="5628c-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="5628c-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5628c-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5628c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5628c-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5628c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5628c-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5628c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5628c-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5628c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5628c-111">語法</span><span class="sxs-lookup"><span data-stu-id="5628c-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5628c-112">參數</span><span class="sxs-lookup"><span data-stu-id="5628c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5628c-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5628c-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5628c-114">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="5628c-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="5628c-115">範例： "c： \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="5628c-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5628c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5628c-116">Return value</span></span>

<span data-ttu-id="5628c-117">在成功時傳回0的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="5628c-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="5628c-118">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="5628c-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5628c-119">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="5628c-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5628c-120">**0**</span><span class="sxs-lookup"><span data-stu-id="5628c-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-121">成功。</span><span class="sxs-lookup"><span data-stu-id="5628c-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-122">**2**</span><span class="sxs-lookup"><span data-stu-id="5628c-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-123">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="5628c-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-124">**8**</span><span class="sxs-lookup"><span data-stu-id="5628c-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-125">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="5628c-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-126">**9**</span><span class="sxs-lookup"><span data-stu-id="5628c-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-127">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="5628c-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-128">**10**</span><span class="sxs-lookup"><span data-stu-id="5628c-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-129">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="5628c-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-130">**11**</span><span class="sxs-lookup"><span data-stu-id="5628c-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-131">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="5628c-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-132">**12**</span><span class="sxs-lookup"><span data-stu-id="5628c-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-133">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="5628c-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-134">**13**</span><span class="sxs-lookup"><span data-stu-id="5628c-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-135">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="5628c-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-136">**14**</span><span class="sxs-lookup"><span data-stu-id="5628c-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-137">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="5628c-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-138">**15**</span><span class="sxs-lookup"><span data-stu-id="5628c-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-139">共用違規。</span><span class="sxs-lookup"><span data-stu-id="5628c-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-140">**16**</span><span class="sxs-lookup"><span data-stu-id="5628c-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-141">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="5628c-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-142">**17**</span><span class="sxs-lookup"><span data-stu-id="5628c-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-143">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="5628c-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="5628c-144">**21**</span><span class="sxs-lookup"><span data-stu-id="5628c-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5628c-145">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="5628c-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5628c-146">備註</span><span class="sxs-lookup"><span data-stu-id="5628c-146">Remarks</span></span>

<span data-ttu-id="5628c-147">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **重新命名** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="5628c-147">The **Rename** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="5628c-148">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5628c-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5628c-149">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5628c-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5628c-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="5628c-150">Requirements</span></span>



| <span data-ttu-id="5628c-151">需求</span><span class="sxs-lookup"><span data-stu-id="5628c-151">Requirement</span></span> | <span data-ttu-id="5628c-152">值</span><span class="sxs-lookup"><span data-stu-id="5628c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5628c-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5628c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5628c-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5628c-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5628c-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5628c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5628c-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5628c-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5628c-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="5628c-157">Namespace</span></span><br/>                | <span data-ttu-id="5628c-158">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5628c-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5628c-159">MOF</span><span class="sxs-lookup"><span data-stu-id="5628c-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5628c-160"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5628c-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5628c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="5628c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5628c-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5628c-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5628c-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5628c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5628c-164">CIM \_ 資料檔案</span><span class="sxs-lookup"><span data-stu-id="5628c-164">CIM\_DataFile</span></span>](rename-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="5628c-165">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="5628c-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="5628c-166">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="5628c-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="5628c-167">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="5628c-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

