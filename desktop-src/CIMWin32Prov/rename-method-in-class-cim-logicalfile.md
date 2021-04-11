---
description: 重新命名方法會將邏輯檔案重新命名 (或在物件路徑中指定的目錄) 。 如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111249"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="55c5b-104">CIM LogicalFile 類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="55c5b-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="55c5b-105">**重新命名** 方法會將邏輯檔案重新命名 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="55c5b-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="55c5b-106">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="55c5b-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55c5b-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="55c5b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55c5b-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="55c5b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55c5b-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="55c5b-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55c5b-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="55c5b-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55c5b-111">語法</span><span class="sxs-lookup"><span data-stu-id="55c5b-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="55c5b-112">參數</span><span class="sxs-lookup"><span data-stu-id="55c5b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c5b-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55c5b-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-114">完整的新檔案 (或目錄) 名稱。</span><span class="sxs-lookup"><span data-stu-id="55c5b-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="55c5b-115">範例： "c： \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="55c5b-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c5b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="55c5b-116">Return value</span></span>

<span data-ttu-id="55c5b-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="55c5b-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="55c5b-118">「成功」</span><span class="sxs-lookup"><span data-stu-id="55c5b-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-119">0</span><span class="sxs-lookup"><span data-stu-id="55c5b-119">0</span></span>

<span data-ttu-id="55c5b-120">成功。</span><span class="sxs-lookup"><span data-stu-id="55c5b-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-121">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="55c5b-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-122">2</span><span class="sxs-lookup"><span data-stu-id="55c5b-122">2</span></span>

<span data-ttu-id="55c5b-123">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="55c5b-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-124">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="55c5b-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-125">8</span><span class="sxs-lookup"><span data-stu-id="55c5b-125">8</span></span>

<span data-ttu-id="55c5b-126">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="55c5b-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-127">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="55c5b-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-128">9</span><span class="sxs-lookup"><span data-stu-id="55c5b-128">9</span></span>

<span data-ttu-id="55c5b-129">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="55c5b-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-130">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="55c5b-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-131">10</span><span class="sxs-lookup"><span data-stu-id="55c5b-131">10</span></span>

<span data-ttu-id="55c5b-132">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="55c5b-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-133">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="55c5b-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-134">11</span><span class="sxs-lookup"><span data-stu-id="55c5b-134">11</span></span>

<span data-ttu-id="55c5b-135">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="55c5b-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-136">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="55c5b-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-137">12</span><span class="sxs-lookup"><span data-stu-id="55c5b-137">12</span></span>

<span data-ttu-id="55c5b-138">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="55c5b-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-139">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="55c5b-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-140">13</span><span class="sxs-lookup"><span data-stu-id="55c5b-140">13</span></span>

<span data-ttu-id="55c5b-141">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="55c5b-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-142">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="55c5b-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-143">14</span><span class="sxs-lookup"><span data-stu-id="55c5b-143">14</span></span>

<span data-ttu-id="55c5b-144">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="55c5b-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-145">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="55c5b-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-146">15</span><span class="sxs-lookup"><span data-stu-id="55c5b-146">15</span></span>

<span data-ttu-id="55c5b-147">共用違規。</span><span class="sxs-lookup"><span data-stu-id="55c5b-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-148">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="55c5b-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-149">16</span><span class="sxs-lookup"><span data-stu-id="55c5b-149">16</span></span>

<span data-ttu-id="55c5b-150">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="55c5b-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-151">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="55c5b-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-152">17</span><span class="sxs-lookup"><span data-stu-id="55c5b-152">17</span></span>

<span data-ttu-id="55c5b-153">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="55c5b-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="55c5b-154">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="55c5b-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55c5b-155">21</span><span class="sxs-lookup"><span data-stu-id="55c5b-155">21</span></span>

<span data-ttu-id="55c5b-156">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="55c5b-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55c5b-157">備註</span><span class="sxs-lookup"><span data-stu-id="55c5b-157">Remarks</span></span>

<span data-ttu-id="55c5b-158">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="55c5b-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="55c5b-159">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="55c5b-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="55c5b-160">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="55c5b-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55c5b-161">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="55c5b-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c5b-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="55c5b-162">Requirements</span></span>



| <span data-ttu-id="55c5b-163">需求</span><span class="sxs-lookup"><span data-stu-id="55c5b-163">Requirement</span></span> | <span data-ttu-id="55c5b-164">值</span><span class="sxs-lookup"><span data-stu-id="55c5b-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55c5b-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55c5b-165">Minimum supported client</span></span><br/> | <span data-ttu-id="55c5b-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55c5b-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55c5b-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55c5b-167">Minimum supported server</span></span><br/> | <span data-ttu-id="55c5b-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55c5b-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55c5b-169">命名空間</span><span class="sxs-lookup"><span data-stu-id="55c5b-169">Namespace</span></span><br/>                | <span data-ttu-id="55c5b-170">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55c5b-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55c5b-171">MOF</span><span class="sxs-lookup"><span data-stu-id="55c5b-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55c5b-172"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55c5b-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55c5b-173">DLL</span><span class="sxs-lookup"><span data-stu-id="55c5b-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55c5b-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55c5b-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c5b-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55c5b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c5b-176">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="55c5b-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="55c5b-177">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="55c5b-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

