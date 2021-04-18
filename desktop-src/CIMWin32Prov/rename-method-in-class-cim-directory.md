---
description: 重新命名在物件路徑中指定的邏輯檔案 (或目錄) 。 如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: CIM_Directory 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468452"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="43829-104">CIM 目錄類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="43829-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="43829-105">**重新命名** 方法會將邏輯檔案重新命名 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="43829-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="43829-106">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="43829-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="43829-107">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="43829-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43829-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="43829-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="43829-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="43829-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="43829-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="43829-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43829-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="43829-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43829-112">語法</span><span class="sxs-lookup"><span data-stu-id="43829-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="43829-113">參數</span><span class="sxs-lookup"><span data-stu-id="43829-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43829-114">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43829-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43829-115">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="43829-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="43829-116">範例： "c： \\ temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="43829-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43829-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="43829-117">Return value</span></span>

<span data-ttu-id="43829-118">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="43829-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="43829-119">**0**</span><span class="sxs-lookup"><span data-stu-id="43829-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="43829-120">成功。</span><span class="sxs-lookup"><span data-stu-id="43829-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="43829-121">**2**</span><span class="sxs-lookup"><span data-stu-id="43829-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="43829-122">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="43829-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="43829-123">**8**</span><span class="sxs-lookup"><span data-stu-id="43829-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="43829-124">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="43829-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="43829-125">**9**</span><span class="sxs-lookup"><span data-stu-id="43829-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="43829-126">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="43829-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="43829-127">**10**</span><span class="sxs-lookup"><span data-stu-id="43829-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="43829-128">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="43829-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="43829-129">**11**</span><span class="sxs-lookup"><span data-stu-id="43829-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="43829-130">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="43829-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="43829-131">**12**</span><span class="sxs-lookup"><span data-stu-id="43829-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="43829-132">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="43829-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="43829-133">**13**</span><span class="sxs-lookup"><span data-stu-id="43829-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="43829-134">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="43829-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="43829-135">**14**</span><span class="sxs-lookup"><span data-stu-id="43829-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="43829-136">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="43829-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="43829-137">**15**</span><span class="sxs-lookup"><span data-stu-id="43829-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="43829-138">共用違規。</span><span class="sxs-lookup"><span data-stu-id="43829-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="43829-139">**16**</span><span class="sxs-lookup"><span data-stu-id="43829-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="43829-140">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="43829-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="43829-141">**17**</span><span class="sxs-lookup"><span data-stu-id="43829-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="43829-142">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="43829-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="43829-143">**21**</span><span class="sxs-lookup"><span data-stu-id="43829-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="43829-144">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="43829-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43829-145">備註</span><span class="sxs-lookup"><span data-stu-id="43829-145">Remarks</span></span>

<span data-ttu-id="43829-146">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="43829-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="43829-147">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="43829-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="43829-148">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="43829-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="43829-149">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="43829-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="43829-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="43829-150">Requirements</span></span>



| <span data-ttu-id="43829-151">需求</span><span class="sxs-lookup"><span data-stu-id="43829-151">Requirement</span></span> | <span data-ttu-id="43829-152">值</span><span class="sxs-lookup"><span data-stu-id="43829-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43829-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43829-153">Minimum supported client</span></span><br/> | <span data-ttu-id="43829-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43829-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43829-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43829-155">Minimum supported server</span></span><br/> | <span data-ttu-id="43829-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43829-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43829-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="43829-157">Namespace</span></span><br/>                | <span data-ttu-id="43829-158">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="43829-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43829-159">MOF</span><span class="sxs-lookup"><span data-stu-id="43829-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43829-160"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="43829-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43829-161">DLL</span><span class="sxs-lookup"><span data-stu-id="43829-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43829-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43829-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43829-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43829-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43829-164">CIM \_ 目錄</span><span class="sxs-lookup"><span data-stu-id="43829-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="43829-165">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="43829-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

