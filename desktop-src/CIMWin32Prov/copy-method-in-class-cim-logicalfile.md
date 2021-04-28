---
description: CIM_LogicalFile 類別的 copy 方法-Copy 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: CIM_LogicalFile 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089726"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="d4ec1-103">CIM LogicalFile 類別的 Copy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d4ec1-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="d4ec1-104">**Copy** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4ec1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d4ec1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d4ec1-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d4ec1-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ec1-109">語法</span><span class="sxs-lookup"><span data-stu-id="d4ec1-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d4ec1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4ec1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ec1-111">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ec1-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-112">目的地檔 (或目錄) 的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="d4ec1-113">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="d4ec1-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ec1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4ec1-114">Return value</span></span>

<span data-ttu-id="d4ec1-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d4ec1-116">「成功」</span><span class="sxs-lookup"><span data-stu-id="d4ec1-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-117">0</span><span class="sxs-lookup"><span data-stu-id="d4ec1-117">0</span></span>

<span data-ttu-id="d4ec1-118">成功。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-119">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-120">2</span><span class="sxs-lookup"><span data-stu-id="d4ec1-120">2</span></span>

<span data-ttu-id="d4ec1-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-122">**未指定的失敗**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-123">8</span><span class="sxs-lookup"><span data-stu-id="d4ec1-123">8</span></span>

<span data-ttu-id="d4ec1-124">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-125">**不正確物件**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-126">9</span><span class="sxs-lookup"><span data-stu-id="d4ec1-126">9</span></span>

<span data-ttu-id="d4ec1-127">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-128">**物件已存在**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-129">10</span><span class="sxs-lookup"><span data-stu-id="d4ec1-129">10</span></span>

<span data-ttu-id="d4ec1-130">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-131">**檔案系統非 NTFS**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-132">11</span><span class="sxs-lookup"><span data-stu-id="d4ec1-132">11</span></span>

<span data-ttu-id="d4ec1-133">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-134">**平臺非 NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-135">12</span><span class="sxs-lookup"><span data-stu-id="d4ec1-135">12</span></span>

<span data-ttu-id="d4ec1-136">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-137">**磁片磁碟機不相同**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-138">13</span><span class="sxs-lookup"><span data-stu-id="d4ec1-138">13</span></span>

<span data-ttu-id="d4ec1-139">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-140">**目錄非空白**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-141">14</span><span class="sxs-lookup"><span data-stu-id="d4ec1-141">14</span></span>

<span data-ttu-id="d4ec1-142">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-143">**共用違規**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-144">15</span><span class="sxs-lookup"><span data-stu-id="d4ec1-144">15</span></span>

<span data-ttu-id="d4ec1-145">共用違規。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-146">**不正確開機檔案**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-147">16</span><span class="sxs-lookup"><span data-stu-id="d4ec1-147">16</span></span>

<span data-ttu-id="d4ec1-148">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-149">**未保留許可權**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-150">17</span><span class="sxs-lookup"><span data-stu-id="d4ec1-150">17</span></span>

<span data-ttu-id="d4ec1-151">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="d4ec1-152">**參數不正確**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d4ec1-153">21</span><span class="sxs-lookup"><span data-stu-id="d4ec1-153">21</span></span>

<span data-ttu-id="d4ec1-154">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4ec1-155">備註</span><span class="sxs-lookup"><span data-stu-id="d4ec1-155">Remarks</span></span>

<span data-ttu-id="d4ec1-156">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d4ec1-157">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d4ec1-158">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d4ec1-159">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ec1-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ec1-160">Requirements</span></span>



| <span data-ttu-id="d4ec1-161">需求</span><span class="sxs-lookup"><span data-stu-id="d4ec1-161">Requirement</span></span> | <span data-ttu-id="d4ec1-162">值</span><span class="sxs-lookup"><span data-stu-id="d4ec1-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ec1-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4ec1-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ec1-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4ec1-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4ec1-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4ec1-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ec1-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4ec1-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4ec1-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="d4ec1-167">Namespace</span></span><br/>                | <span data-ttu-id="d4ec1-168">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d4ec1-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4ec1-169">MOF</span><span class="sxs-lookup"><span data-stu-id="d4ec1-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4ec1-170"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4ec1-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4ec1-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ec1-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ec1-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ec1-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ec1-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ec1-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ec1-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="d4ec1-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="d4ec1-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="d4ec1-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

