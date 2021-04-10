---
description: 取得物件路徑中指定之邏輯目錄專案檔的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: CIM_Directory 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110169"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="f01a2-104">CIM 目錄類別的 TakeOwnerShipEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f01a2-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="f01a2-105">**TakeOwnerShipEx** 方法會取得物件路徑中指定之邏輯目錄專案檔的擁有權。</span><span class="sxs-lookup"><span data-stu-id="f01a2-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="f01a2-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="f01a2-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="f01a2-107">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="f01a2-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f01a2-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f01a2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f01a2-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f01a2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f01a2-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f01a2-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f01a2-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f01a2-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f01a2-112">語法</span><span class="sxs-lookup"><span data-stu-id="f01a2-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f01a2-113">參數</span><span class="sxs-lookup"><span data-stu-id="f01a2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01a2-114">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f01a2-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a2-115">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f01a2-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="f01a2-116">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="f01a2-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f01a2-117">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f01a2-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a2-118">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="f01a2-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="f01a2-119">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="f01a2-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f01a2-120">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="f01a2-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="f01a2-121">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f01a2-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f01a2-122">若 **為 True**，則會以遞迴方式將方法套用至 [**CIM \_ 目錄**](cim-directory.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="f01a2-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="f01a2-123">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="f01a2-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01a2-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f01a2-124">Return value</span></span>

<span data-ttu-id="f01a2-125">在成功時傳回0的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="f01a2-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-126">0</span><span class="sxs-lookup"><span data-stu-id="f01a2-126">0</span></span>

<span data-ttu-id="f01a2-127">成功。</span><span class="sxs-lookup"><span data-stu-id="f01a2-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-128">2</span><span class="sxs-lookup"><span data-stu-id="f01a2-128">2</span></span>

<span data-ttu-id="f01a2-129">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="f01a2-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-130">8</span><span class="sxs-lookup"><span data-stu-id="f01a2-130">8</span></span>

<span data-ttu-id="f01a2-131">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="f01a2-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-132">9</span><span class="sxs-lookup"><span data-stu-id="f01a2-132">9</span></span>

<span data-ttu-id="f01a2-133">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="f01a2-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-134">10</span><span class="sxs-lookup"><span data-stu-id="f01a2-134">10</span></span>

<span data-ttu-id="f01a2-135">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="f01a2-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-136">11</span><span class="sxs-lookup"><span data-stu-id="f01a2-136">11</span></span>

<span data-ttu-id="f01a2-137">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="f01a2-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-138">12</span><span class="sxs-lookup"><span data-stu-id="f01a2-138">12</span></span>

<span data-ttu-id="f01a2-139">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="f01a2-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-140">13</span><span class="sxs-lookup"><span data-stu-id="f01a2-140">13</span></span>

<span data-ttu-id="f01a2-141">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="f01a2-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-142">14</span><span class="sxs-lookup"><span data-stu-id="f01a2-142">14</span></span>

<span data-ttu-id="f01a2-143">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="f01a2-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-144">15</span><span class="sxs-lookup"><span data-stu-id="f01a2-144">15</span></span>

<span data-ttu-id="f01a2-145">共用違規。</span><span class="sxs-lookup"><span data-stu-id="f01a2-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-146">16</span><span class="sxs-lookup"><span data-stu-id="f01a2-146">16</span></span>

<span data-ttu-id="f01a2-147">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="f01a2-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-148">17</span><span class="sxs-lookup"><span data-stu-id="f01a2-148">17</span></span>

<span data-ttu-id="f01a2-149">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="f01a2-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f01a2-150">21</span><span class="sxs-lookup"><span data-stu-id="f01a2-150">21</span></span>

<span data-ttu-id="f01a2-151">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="f01a2-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f01a2-152">備註</span><span class="sxs-lookup"><span data-stu-id="f01a2-152">Remarks</span></span>

<span data-ttu-id="f01a2-153">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f01a2-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f01a2-154">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="f01a2-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f01a2-155">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f01a2-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f01a2-156">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f01a2-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="f01a2-157">範例</span><span class="sxs-lookup"><span data-stu-id="f01a2-157">Examples</span></span>

<span data-ttu-id="f01a2-158">下列 Visual Basic 腳本程式碼會呼叫 **TakeOwnerShipEx** 方法來取得 C： temp 資料夾的擁有權 \\ 。</span><span class="sxs-lookup"><span data-stu-id="f01a2-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="f01a2-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="f01a2-159">Requirements</span></span>



| <span data-ttu-id="f01a2-160">需求</span><span class="sxs-lookup"><span data-stu-id="f01a2-160">Requirement</span></span> | <span data-ttu-id="f01a2-161">值</span><span class="sxs-lookup"><span data-stu-id="f01a2-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f01a2-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f01a2-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f01a2-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f01a2-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f01a2-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f01a2-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f01a2-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f01a2-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f01a2-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="f01a2-166">Namespace</span></span><br/>                | <span data-ttu-id="f01a2-167">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f01a2-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f01a2-168">MOF</span><span class="sxs-lookup"><span data-stu-id="f01a2-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f01a2-169"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f01a2-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f01a2-170">DLL</span><span class="sxs-lookup"><span data-stu-id="f01a2-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f01a2-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f01a2-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f01a2-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f01a2-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01a2-173">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="f01a2-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="f01a2-174">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="f01a2-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

