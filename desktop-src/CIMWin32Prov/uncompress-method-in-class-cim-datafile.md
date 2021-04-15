---
description: Uncompresses 邏輯資料檔案 (或在物件路徑中指定的目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: CIM_DataFile 類別的解壓縮方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24495c94cca0eb6b99bc209cad8f25fac8f66896
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468077"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a><span data-ttu-id="59b92-104">CIM \_ 資料檔案類別的解壓縮方法</span><span class="sxs-lookup"><span data-stu-id="59b92-104">Uncompress method of the CIM\_DataFile class</span></span>

<span data-ttu-id="59b92-105">**解壓縮** 方法會 uncompresses 邏輯資料檔案 (或物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="59b92-105">The **Uncompress** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="59b92-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="59b92-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59b92-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="59b92-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="59b92-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="59b92-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="59b92-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="59b92-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="59b92-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="59b92-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="59b92-111">語法</span><span class="sxs-lookup"><span data-stu-id="59b92-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="59b92-112">參數</span><span class="sxs-lookup"><span data-stu-id="59b92-112">Parameters</span></span>

<span data-ttu-id="59b92-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="59b92-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59b92-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="59b92-114">Return value</span></span>

<span data-ttu-id="59b92-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="59b92-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="59b92-116">如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="59b92-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="59b92-117">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="59b92-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="59b92-118">**0**</span><span class="sxs-lookup"><span data-stu-id="59b92-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-119">成功。</span><span class="sxs-lookup"><span data-stu-id="59b92-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-120">**2**</span><span class="sxs-lookup"><span data-stu-id="59b92-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="59b92-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-122">**8**</span><span class="sxs-lookup"><span data-stu-id="59b92-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-123">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="59b92-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-124">**9**</span><span class="sxs-lookup"><span data-stu-id="59b92-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-125">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="59b92-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-126">**10**</span><span class="sxs-lookup"><span data-stu-id="59b92-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-127">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="59b92-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-128">**11**</span><span class="sxs-lookup"><span data-stu-id="59b92-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-129">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="59b92-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-130">**12**</span><span class="sxs-lookup"><span data-stu-id="59b92-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-131">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="59b92-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-132">**13**</span><span class="sxs-lookup"><span data-stu-id="59b92-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-133">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="59b92-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-134">**14**</span><span class="sxs-lookup"><span data-stu-id="59b92-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-135">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="59b92-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-136">**15**</span><span class="sxs-lookup"><span data-stu-id="59b92-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-137">共用違規。</span><span class="sxs-lookup"><span data-stu-id="59b92-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-138">**16**</span><span class="sxs-lookup"><span data-stu-id="59b92-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-139">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="59b92-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-140">**17**</span><span class="sxs-lookup"><span data-stu-id="59b92-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-141">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="59b92-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="59b92-142">**21**</span><span class="sxs-lookup"><span data-stu-id="59b92-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="59b92-143">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="59b92-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59b92-144">備註</span><span class="sxs-lookup"><span data-stu-id="59b92-144">Remarks</span></span>

<span data-ttu-id="59b92-145">[**CIM \_ 資料檔案**](cim-datafile.md)中的 **解壓縮** 方法是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="59b92-145">The **Uncompress** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="59b92-146">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="59b92-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="59b92-147">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="59b92-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b92-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="59b92-148">Requirements</span></span>



| <span data-ttu-id="59b92-149">需求</span><span class="sxs-lookup"><span data-stu-id="59b92-149">Requirement</span></span> | <span data-ttu-id="59b92-150">值</span><span class="sxs-lookup"><span data-stu-id="59b92-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59b92-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59b92-151">Minimum supported client</span></span><br/> | <span data-ttu-id="59b92-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59b92-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="59b92-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59b92-153">Minimum supported server</span></span><br/> | <span data-ttu-id="59b92-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59b92-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="59b92-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="59b92-155">Namespace</span></span><br/>                | <span data-ttu-id="59b92-156">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="59b92-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="59b92-157">MOF</span><span class="sxs-lookup"><span data-stu-id="59b92-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59b92-158"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="59b92-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="59b92-159">DLL</span><span class="sxs-lookup"><span data-stu-id="59b92-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59b92-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59b92-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b92-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59b92-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b92-162">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="59b92-162">**CIM\_DataFile**</span></span>](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="59b92-163">**CIM \_ 資料檔案**</span><span class="sxs-lookup"><span data-stu-id="59b92-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="59b92-164">WMI 工作：檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="59b92-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="59b92-165">**檔案和目錄存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="59b92-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

