---
description: TakeOwnerShip 方法會取得物件路徑中所指定之邏輯檔案的擁有權。
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: CIM_Directory 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc68e974c98405f03c4bbfb45f02fdf78bf65127
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191038"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="406ce-103">CIM 目錄類別的 TakeOwnerShip 方法 \_</span><span class="sxs-lookup"><span data-stu-id="406ce-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="406ce-104">**TakeOwnerShip** 方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="406ce-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="406ce-105">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="406ce-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="406ce-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="406ce-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="406ce-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="406ce-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="406ce-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="406ce-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="406ce-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="406ce-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="406ce-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="406ce-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="406ce-111">語法</span><span class="sxs-lookup"><span data-stu-id="406ce-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="406ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="406ce-112">Parameters</span></span>

<span data-ttu-id="406ce-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="406ce-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="406ce-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="406ce-114">Return value</span></span>

<span data-ttu-id="406ce-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="406ce-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="406ce-116">**0**</span><span class="sxs-lookup"><span data-stu-id="406ce-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-117">成功。</span><span class="sxs-lookup"><span data-stu-id="406ce-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-118">**2**</span><span class="sxs-lookup"><span data-stu-id="406ce-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-119">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="406ce-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-120">**8**</span><span class="sxs-lookup"><span data-stu-id="406ce-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-121">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="406ce-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-122">**9**</span><span class="sxs-lookup"><span data-stu-id="406ce-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-123">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="406ce-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-124">**10**</span><span class="sxs-lookup"><span data-stu-id="406ce-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-125">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="406ce-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-126">**11**</span><span class="sxs-lookup"><span data-stu-id="406ce-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-127">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="406ce-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-128">**12**</span><span class="sxs-lookup"><span data-stu-id="406ce-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-129">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="406ce-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-130">**13**</span><span class="sxs-lookup"><span data-stu-id="406ce-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-131">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="406ce-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-132">**14**</span><span class="sxs-lookup"><span data-stu-id="406ce-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-133">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="406ce-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-134">**15**</span><span class="sxs-lookup"><span data-stu-id="406ce-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-135">共用違規。</span><span class="sxs-lookup"><span data-stu-id="406ce-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-136">**16**</span><span class="sxs-lookup"><span data-stu-id="406ce-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-137">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="406ce-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-138">**17**</span><span class="sxs-lookup"><span data-stu-id="406ce-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-139">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="406ce-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="406ce-140">**21**</span><span class="sxs-lookup"><span data-stu-id="406ce-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="406ce-141">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="406ce-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="406ce-142">備註</span><span class="sxs-lookup"><span data-stu-id="406ce-142">Remarks</span></span>

<span data-ttu-id="406ce-143">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="406ce-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="406ce-144">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="406ce-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="406ce-145">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="406ce-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="406ce-146">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="406ce-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="406ce-147">範例</span><span class="sxs-lookup"><span data-stu-id="406ce-147">Examples</span></span>

<span data-ttu-id="406ce-148">下列 Visual Basic 腳本程式碼會呼叫 **TakeOwnerShip** 方法來取得 C： temp 資料夾的擁有權 \\ 。</span><span class="sxs-lookup"><span data-stu-id="406ce-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="406ce-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="406ce-149">Requirements</span></span>



| <span data-ttu-id="406ce-150">需求</span><span class="sxs-lookup"><span data-stu-id="406ce-150">Requirement</span></span> | <span data-ttu-id="406ce-151">值</span><span class="sxs-lookup"><span data-stu-id="406ce-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="406ce-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="406ce-152">Minimum supported client</span></span><br/> | <span data-ttu-id="406ce-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="406ce-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="406ce-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="406ce-154">Minimum supported server</span></span><br/> | <span data-ttu-id="406ce-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="406ce-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="406ce-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="406ce-156">Namespace</span></span><br/>                | <span data-ttu-id="406ce-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="406ce-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="406ce-158">MOF</span><span class="sxs-lookup"><span data-stu-id="406ce-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="406ce-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="406ce-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="406ce-160">DLL</span><span class="sxs-lookup"><span data-stu-id="406ce-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="406ce-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="406ce-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="406ce-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="406ce-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406ce-163">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="406ce-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="406ce-164">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="406ce-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

