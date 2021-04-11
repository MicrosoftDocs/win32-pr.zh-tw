---
description: Uncompresses 邏輯目錄專案檔 (或在物件路徑中指定的目錄) 。 這個方法繼承自 CIM \_ LogicalFile。
ms.assetid: da3616d0-ce45-4e9a-a570-ca9e6bd0a4fa
ms.tgt_platform: multiple
title: CIM_Directory 類別的解壓縮方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d852305d9153fa61f33168303ccb791caad00f28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936170"
---
# <a name="uncompress-method-of-the-cim_directory-class"></a><span data-ttu-id="a202f-104">CIM 目錄類別的解壓縮方法 \_</span><span class="sxs-lookup"><span data-stu-id="a202f-104">Uncompress method of the CIM\_Directory class</span></span>

<span data-ttu-id="a202f-105">**解壓縮** 方法會 uncompresses 邏輯目錄專案檔 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="a202f-105">The **Uncompress** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="a202f-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="a202f-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a202f-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a202f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a202f-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a202f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a202f-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a202f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a202f-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a202f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a202f-111">語法</span><span class="sxs-lookup"><span data-stu-id="a202f-111">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="a202f-112">參數</span><span class="sxs-lookup"><span data-stu-id="a202f-112">Parameters</span></span>

<span data-ttu-id="a202f-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a202f-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a202f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a202f-114">Return value</span></span>

<span data-ttu-id="a202f-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a202f-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a202f-116">**0**</span><span class="sxs-lookup"><span data-stu-id="a202f-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-117">成功。</span><span class="sxs-lookup"><span data-stu-id="a202f-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-118">**2**</span><span class="sxs-lookup"><span data-stu-id="a202f-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-119">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a202f-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-120">**8**</span><span class="sxs-lookup"><span data-stu-id="a202f-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-121">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="a202f-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-122">**9**</span><span class="sxs-lookup"><span data-stu-id="a202f-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-123">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="a202f-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-124">**10**</span><span class="sxs-lookup"><span data-stu-id="a202f-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-125">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="a202f-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-126">**11**</span><span class="sxs-lookup"><span data-stu-id="a202f-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-127">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="a202f-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-128">**12**</span><span class="sxs-lookup"><span data-stu-id="a202f-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-129">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="a202f-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-130">**13**</span><span class="sxs-lookup"><span data-stu-id="a202f-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-131">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="a202f-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-132">**14**</span><span class="sxs-lookup"><span data-stu-id="a202f-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-133">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="a202f-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-134">**15**</span><span class="sxs-lookup"><span data-stu-id="a202f-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-135">共用違規。</span><span class="sxs-lookup"><span data-stu-id="a202f-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-136">**16**</span><span class="sxs-lookup"><span data-stu-id="a202f-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-137">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="a202f-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-138">**17**</span><span class="sxs-lookup"><span data-stu-id="a202f-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-139">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="a202f-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a202f-140">**21**</span><span class="sxs-lookup"><span data-stu-id="a202f-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a202f-141">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="a202f-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a202f-142">備註</span><span class="sxs-lookup"><span data-stu-id="a202f-142">Remarks</span></span>

<span data-ttu-id="a202f-143">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a202f-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a202f-144">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a202f-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a202f-145">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a202f-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a202f-146">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a202f-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a202f-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="a202f-147">Requirements</span></span>



| <span data-ttu-id="a202f-148">需求</span><span class="sxs-lookup"><span data-stu-id="a202f-148">Requirement</span></span> | <span data-ttu-id="a202f-149">值</span><span class="sxs-lookup"><span data-stu-id="a202f-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a202f-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a202f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a202f-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a202f-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a202f-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a202f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a202f-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a202f-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a202f-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="a202f-154">Namespace</span></span><br/>                | <span data-ttu-id="a202f-155">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a202f-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a202f-156">MOF</span><span class="sxs-lookup"><span data-stu-id="a202f-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a202f-157"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a202f-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a202f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="a202f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a202f-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a202f-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a202f-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a202f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a202f-161">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="a202f-161">**CIM\_Directory**</span></span>](uncompress-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="a202f-162">**CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="a202f-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

