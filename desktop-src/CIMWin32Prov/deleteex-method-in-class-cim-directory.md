---
description: CIM_Directory 類別的 DeleteEx 方法-DeleteEx 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。 這個方法是 Delete 方法的擴充版本，會繼承自 CIM \_ LogicalFile。
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: CIM_Directory 類別的 DeleteEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a3704507405ebb2d310ed7341cd1db174e00588
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097096"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a><span data-ttu-id="0fe93-104">CIM 目錄類別的 DeleteEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0fe93-104">DeleteEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="0fe93-105">**DeleteEx** 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0fe93-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0fe93-106">這個方法是 [**Delete**](delete-method-in-class-cim-directory.md) 方法的擴充版本，會繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="0fe93-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fe93-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0fe93-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0fe93-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0fe93-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0fe93-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0fe93-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0fe93-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0fe93-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe93-111">語法</span><span class="sxs-lookup"><span data-stu-id="0fe93-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0fe93-112">參數</span><span class="sxs-lookup"><span data-stu-id="0fe93-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fe93-113">*StopFileName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0fe93-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fe93-114">字串，代表方法失敗 (或目錄) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fe93-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0fe93-115">如果方法成功，則此參數為 null。</span><span class="sxs-lookup"><span data-stu-id="0fe93-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0fe93-116">*StartFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0fe93-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fe93-117">字串，表示要作為此方法起點的子檔 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="0fe93-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="0fe93-118">一般而言，此參數是 *StopFileName* 參數，指定上一次方法呼叫發生錯誤的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="0fe93-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0fe93-119">如果這個參數是 null，則會在 [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) 呼叫中指定的檔案 (或目錄) 上執行作業。</span><span class="sxs-lookup"><span data-stu-id="0fe93-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fe93-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fe93-120">Return value</span></span>

<span data-ttu-id="0fe93-121">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="0fe93-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-122">0</span><span class="sxs-lookup"><span data-stu-id="0fe93-122">0</span></span>

<span data-ttu-id="0fe93-123">成功。</span><span class="sxs-lookup"><span data-stu-id="0fe93-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-124">2</span><span class="sxs-lookup"><span data-stu-id="0fe93-124">2</span></span>

<span data-ttu-id="0fe93-125">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0fe93-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-126">8</span><span class="sxs-lookup"><span data-stu-id="0fe93-126">8</span></span>

<span data-ttu-id="0fe93-127">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="0fe93-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-128">9</span><span class="sxs-lookup"><span data-stu-id="0fe93-128">9</span></span>

<span data-ttu-id="0fe93-129">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="0fe93-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-130">10</span><span class="sxs-lookup"><span data-stu-id="0fe93-130">10</span></span>

<span data-ttu-id="0fe93-131">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="0fe93-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-132">11</span><span class="sxs-lookup"><span data-stu-id="0fe93-132">11</span></span>

<span data-ttu-id="0fe93-133">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="0fe93-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-134">12</span><span class="sxs-lookup"><span data-stu-id="0fe93-134">12</span></span>

<span data-ttu-id="0fe93-135">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="0fe93-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-136">13</span><span class="sxs-lookup"><span data-stu-id="0fe93-136">13</span></span>

<span data-ttu-id="0fe93-137">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="0fe93-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-138">14</span><span class="sxs-lookup"><span data-stu-id="0fe93-138">14</span></span>

<span data-ttu-id="0fe93-139">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="0fe93-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-140">15</span><span class="sxs-lookup"><span data-stu-id="0fe93-140">15</span></span>

<span data-ttu-id="0fe93-141">共用違規。</span><span class="sxs-lookup"><span data-stu-id="0fe93-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-142">16</span><span class="sxs-lookup"><span data-stu-id="0fe93-142">16</span></span>

<span data-ttu-id="0fe93-143">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="0fe93-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-144">17</span><span class="sxs-lookup"><span data-stu-id="0fe93-144">17</span></span>

<span data-ttu-id="0fe93-145">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="0fe93-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0fe93-146">21</span><span class="sxs-lookup"><span data-stu-id="0fe93-146">21</span></span>

<span data-ttu-id="0fe93-147">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="0fe93-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fe93-148">備註</span><span class="sxs-lookup"><span data-stu-id="0fe93-148">Remarks</span></span>

<span data-ttu-id="0fe93-149">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0fe93-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0fe93-150">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="0fe93-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0fe93-151">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0fe93-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0fe93-152">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0fe93-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe93-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fe93-153">Requirements</span></span>



| <span data-ttu-id="0fe93-154">需求</span><span class="sxs-lookup"><span data-stu-id="0fe93-154">Requirement</span></span> | <span data-ttu-id="0fe93-155">值</span><span class="sxs-lookup"><span data-stu-id="0fe93-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe93-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fe93-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe93-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fe93-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fe93-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fe93-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe93-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fe93-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fe93-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="0fe93-160">Namespace</span></span><br/>                | <span data-ttu-id="0fe93-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0fe93-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fe93-162">MOF</span><span class="sxs-lookup"><span data-stu-id="0fe93-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fe93-163"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fe93-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fe93-164">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe93-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe93-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe93-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe93-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fe93-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe93-167">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="0fe93-167">CIM\_Directory</span></span>](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="0fe93-168">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="0fe93-168">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

