---
description: Delete 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。
ms.assetid: 04d43ac5-b7e6-409f-999a-577232539c15
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8462d097834015883d47ec3da0d70e517a4ead0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966649"
---
# <a name="delete-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="206b9-103">CIM LogicalFile 類別的 Delete 方法 \_</span><span class="sxs-lookup"><span data-stu-id="206b9-103">Delete method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="206b9-104">**Delete** 方法會刪除物件路徑中指定的邏輯檔案 (或目錄) 。</span><span class="sxs-lookup"><span data-stu-id="206b9-104">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="206b9-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="206b9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="206b9-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="206b9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="206b9-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="206b9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="206b9-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="206b9-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="206b9-109">語法</span><span class="sxs-lookup"><span data-stu-id="206b9-109">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="206b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="206b9-110">Parameters</span></span>

<span data-ttu-id="206b9-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="206b9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="206b9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="206b9-112">Return value</span></span>

<span data-ttu-id="206b9-113">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="206b9-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="206b9-114">「成功」</span><span class="sxs-lookup"><span data-stu-id="206b9-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-115">0</span><span class="sxs-lookup"><span data-stu-id="206b9-115">0</span></span>

<span data-ttu-id="206b9-116">成功。</span><span class="sxs-lookup"><span data-stu-id="206b9-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-117">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="206b9-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-118">2</span><span class="sxs-lookup"><span data-stu-id="206b9-118">2</span></span>

<span data-ttu-id="206b9-119">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="206b9-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-120">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="206b9-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-121">8</span><span class="sxs-lookup"><span data-stu-id="206b9-121">8</span></span>

<span data-ttu-id="206b9-122">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="206b9-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-123">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="206b9-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-124">9</span><span class="sxs-lookup"><span data-stu-id="206b9-124">9</span></span>

<span data-ttu-id="206b9-125">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="206b9-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-126">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="206b9-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-127">10</span><span class="sxs-lookup"><span data-stu-id="206b9-127">10</span></span>

<span data-ttu-id="206b9-128">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="206b9-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-129">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="206b9-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-130">11</span><span class="sxs-lookup"><span data-stu-id="206b9-130">11</span></span>

<span data-ttu-id="206b9-131">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="206b9-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-132">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="206b9-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-133">12</span><span class="sxs-lookup"><span data-stu-id="206b9-133">12</span></span>

<span data-ttu-id="206b9-134">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="206b9-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-135">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="206b9-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-136">13</span><span class="sxs-lookup"><span data-stu-id="206b9-136">13</span></span>

<span data-ttu-id="206b9-137">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="206b9-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-138">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="206b9-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-139">14</span><span class="sxs-lookup"><span data-stu-id="206b9-139">14</span></span>

<span data-ttu-id="206b9-140">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="206b9-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-141">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="206b9-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-142">15</span><span class="sxs-lookup"><span data-stu-id="206b9-142">15</span></span>

<span data-ttu-id="206b9-143">共用違規。</span><span class="sxs-lookup"><span data-stu-id="206b9-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-144">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="206b9-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-145">16</span><span class="sxs-lookup"><span data-stu-id="206b9-145">16</span></span>

<span data-ttu-id="206b9-146">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="206b9-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-147">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="206b9-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-148">17</span><span class="sxs-lookup"><span data-stu-id="206b9-148">17</span></span>

<span data-ttu-id="206b9-149">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="206b9-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="206b9-150">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="206b9-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="206b9-151">21</span><span class="sxs-lookup"><span data-stu-id="206b9-151">21</span></span>

<span data-ttu-id="206b9-152">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="206b9-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="206b9-153">備註</span><span class="sxs-lookup"><span data-stu-id="206b9-153">Remarks</span></span>

<span data-ttu-id="206b9-154">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="206b9-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="206b9-155">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="206b9-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="206b9-156">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="206b9-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="206b9-157">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="206b9-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="206b9-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="206b9-158">Requirements</span></span>



| <span data-ttu-id="206b9-159">需求</span><span class="sxs-lookup"><span data-stu-id="206b9-159">Requirement</span></span> | <span data-ttu-id="206b9-160">值</span><span class="sxs-lookup"><span data-stu-id="206b9-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="206b9-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="206b9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="206b9-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="206b9-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="206b9-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="206b9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="206b9-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="206b9-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="206b9-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="206b9-165">Namespace</span></span><br/>                | <span data-ttu-id="206b9-166">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="206b9-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="206b9-167">MOF</span><span class="sxs-lookup"><span data-stu-id="206b9-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="206b9-168"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="206b9-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="206b9-169">DLL</span><span class="sxs-lookup"><span data-stu-id="206b9-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="206b9-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="206b9-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206b9-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="206b9-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206b9-172">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="206b9-172">CIM\_LogicalFile</span></span>](delete-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="206b9-173">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="206b9-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

