---
description: 取得物件路徑中指定之邏輯裝置檔案的擁有權。 這個方法是 TakeOwnerShip 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 TakeOwnerShipEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847047"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="46788-104">CIM DeviceFile 類別的 TakeOwnerShipEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="46788-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="46788-105">**TakeOwnerShipEx** 方法會取得物件路徑中指定之邏輯裝置檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="46788-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="46788-106">這個方法是 [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="46788-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="46788-107">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="46788-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46788-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="46788-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="46788-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="46788-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="46788-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="46788-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="46788-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="46788-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="46788-112">語法</span><span class="sxs-lookup"><span data-stu-id="46788-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="46788-113">參數</span><span class="sxs-lookup"><span data-stu-id="46788-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46788-114">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46788-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46788-115">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="46788-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="46788-116">如果方法成功，則此參數為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="46788-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="46788-117">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46788-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46788-118">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="46788-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="46788-119">一般而言， *StartFileName* 參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="46788-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="46788-120">如果這個參數是 **null**，則會在 **ExecMethod** 呼叫中指定的檔案或目錄上執行作業。</span><span class="sxs-lookup"><span data-stu-id="46788-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="46788-121">*遞迴* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46788-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46788-122">若 **為 TRUE**，則此方法也會以遞迴方式套用至 [**CIM \_ DeviceFile**](cim-devicefile.md) 實例所指定之目錄中的檔案和目錄。</span><span class="sxs-lookup"><span data-stu-id="46788-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="46788-123">若為檔案實例，則會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="46788-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46788-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="46788-124">Return value</span></span>

<span data-ttu-id="46788-125">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="46788-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="46788-126">0</span><span class="sxs-lookup"><span data-stu-id="46788-126">0</span></span>

<span data-ttu-id="46788-127">成功。</span><span class="sxs-lookup"><span data-stu-id="46788-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-128">2</span><span class="sxs-lookup"><span data-stu-id="46788-128">2</span></span>

<span data-ttu-id="46788-129">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="46788-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-130">8</span><span class="sxs-lookup"><span data-stu-id="46788-130">8</span></span>

<span data-ttu-id="46788-131">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="46788-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-132">9</span><span class="sxs-lookup"><span data-stu-id="46788-132">9</span></span>

<span data-ttu-id="46788-133">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="46788-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-134">10</span><span class="sxs-lookup"><span data-stu-id="46788-134">10</span></span>

<span data-ttu-id="46788-135">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="46788-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-136">11</span><span class="sxs-lookup"><span data-stu-id="46788-136">11</span></span>

<span data-ttu-id="46788-137">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="46788-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-138">12</span><span class="sxs-lookup"><span data-stu-id="46788-138">12</span></span>

<span data-ttu-id="46788-139">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="46788-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-140">13</span><span class="sxs-lookup"><span data-stu-id="46788-140">13</span></span>

<span data-ttu-id="46788-141">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="46788-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-142">14</span><span class="sxs-lookup"><span data-stu-id="46788-142">14</span></span>

<span data-ttu-id="46788-143">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="46788-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-144">15</span><span class="sxs-lookup"><span data-stu-id="46788-144">15</span></span>

<span data-ttu-id="46788-145">共用違規。</span><span class="sxs-lookup"><span data-stu-id="46788-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-146">16</span><span class="sxs-lookup"><span data-stu-id="46788-146">16</span></span>

<span data-ttu-id="46788-147">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="46788-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-148">17</span><span class="sxs-lookup"><span data-stu-id="46788-148">17</span></span>

<span data-ttu-id="46788-149">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="46788-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="46788-150">21</span><span class="sxs-lookup"><span data-stu-id="46788-150">21</span></span>

<span data-ttu-id="46788-151">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="46788-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46788-152">備註</span><span class="sxs-lookup"><span data-stu-id="46788-152">Remarks</span></span>

<span data-ttu-id="46788-153">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="46788-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="46788-154">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="46788-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="46788-155">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="46788-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="46788-156">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="46788-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="46788-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="46788-157">Requirements</span></span>



| <span data-ttu-id="46788-158">需求</span><span class="sxs-lookup"><span data-stu-id="46788-158">Requirement</span></span> | <span data-ttu-id="46788-159">值</span><span class="sxs-lookup"><span data-stu-id="46788-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46788-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46788-160">Minimum supported client</span></span><br/> | <span data-ttu-id="46788-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46788-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46788-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46788-162">Minimum supported server</span></span><br/> | <span data-ttu-id="46788-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46788-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46788-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="46788-164">Namespace</span></span><br/>                | <span data-ttu-id="46788-165">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46788-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46788-166">MOF</span><span class="sxs-lookup"><span data-stu-id="46788-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46788-167"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="46788-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46788-168">DLL</span><span class="sxs-lookup"><span data-stu-id="46788-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46788-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46788-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46788-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46788-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46788-171">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="46788-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="46788-172">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="46788-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

