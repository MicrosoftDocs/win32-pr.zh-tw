---
description: TakeOwnerShip 方法會取得物件路徑中所指定之邏輯檔案的擁有權。 如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510415"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="738d5-104">CIM LogicalFile 類別的 TakeOwnerShip 方法 \_</span><span class="sxs-lookup"><span data-stu-id="738d5-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="738d5-105">**TakeOwnerShip** 方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="738d5-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="738d5-106">如果邏輯檔案是目錄，則此方法會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="738d5-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="738d5-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="738d5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="738d5-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="738d5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="738d5-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="738d5-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="738d5-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="738d5-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="738d5-111">語法</span><span class="sxs-lookup"><span data-stu-id="738d5-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="738d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="738d5-112">Parameters</span></span>

<span data-ttu-id="738d5-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="738d5-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="738d5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="738d5-114">Return value</span></span>

<span data-ttu-id="738d5-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="738d5-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="738d5-116">「成功」</span><span class="sxs-lookup"><span data-stu-id="738d5-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-117">0</span><span class="sxs-lookup"><span data-stu-id="738d5-117">0</span></span>

<span data-ttu-id="738d5-118">成功。</span><span class="sxs-lookup"><span data-stu-id="738d5-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-119">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="738d5-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-120">2</span><span class="sxs-lookup"><span data-stu-id="738d5-120">2</span></span>

<span data-ttu-id="738d5-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="738d5-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-122">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="738d5-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-123">8</span><span class="sxs-lookup"><span data-stu-id="738d5-123">8</span></span>

<span data-ttu-id="738d5-124">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="738d5-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-125">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="738d5-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-126">9</span><span class="sxs-lookup"><span data-stu-id="738d5-126">9</span></span>

<span data-ttu-id="738d5-127">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="738d5-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-128">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="738d5-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-129">10</span><span class="sxs-lookup"><span data-stu-id="738d5-129">10</span></span>

<span data-ttu-id="738d5-130">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="738d5-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-131">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="738d5-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-132">11</span><span class="sxs-lookup"><span data-stu-id="738d5-132">11</span></span>

<span data-ttu-id="738d5-133">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="738d5-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-134">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="738d5-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-135">12</span><span class="sxs-lookup"><span data-stu-id="738d5-135">12</span></span>

<span data-ttu-id="738d5-136">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="738d5-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-137">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="738d5-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-138">13</span><span class="sxs-lookup"><span data-stu-id="738d5-138">13</span></span>

<span data-ttu-id="738d5-139">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="738d5-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-140">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="738d5-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-141">14</span><span class="sxs-lookup"><span data-stu-id="738d5-141">14</span></span>

<span data-ttu-id="738d5-142">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="738d5-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-143">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="738d5-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-144">15</span><span class="sxs-lookup"><span data-stu-id="738d5-144">15</span></span>

<span data-ttu-id="738d5-145">共用違規。</span><span class="sxs-lookup"><span data-stu-id="738d5-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-146">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="738d5-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-147">16</span><span class="sxs-lookup"><span data-stu-id="738d5-147">16</span></span>

<span data-ttu-id="738d5-148">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="738d5-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-149">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="738d5-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-150">17</span><span class="sxs-lookup"><span data-stu-id="738d5-150">17</span></span>

<span data-ttu-id="738d5-151">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="738d5-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="738d5-152">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="738d5-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="738d5-153">21</span><span class="sxs-lookup"><span data-stu-id="738d5-153">21</span></span>

<span data-ttu-id="738d5-154">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="738d5-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="738d5-155">備註</span><span class="sxs-lookup"><span data-stu-id="738d5-155">Remarks</span></span>

<span data-ttu-id="738d5-156">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="738d5-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="738d5-157">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="738d5-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="738d5-158">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="738d5-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="738d5-159">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="738d5-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="738d5-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="738d5-160">Requirements</span></span>



| <span data-ttu-id="738d5-161">需求</span><span class="sxs-lookup"><span data-stu-id="738d5-161">Requirement</span></span> | <span data-ttu-id="738d5-162">值</span><span class="sxs-lookup"><span data-stu-id="738d5-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="738d5-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="738d5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="738d5-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="738d5-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="738d5-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="738d5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="738d5-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="738d5-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="738d5-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="738d5-167">Namespace</span></span><br/>                | <span data-ttu-id="738d5-168">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="738d5-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="738d5-169">MOF</span><span class="sxs-lookup"><span data-stu-id="738d5-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="738d5-170"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="738d5-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="738d5-171">DLL</span><span class="sxs-lookup"><span data-stu-id="738d5-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="738d5-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="738d5-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738d5-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="738d5-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738d5-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="738d5-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="738d5-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="738d5-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

