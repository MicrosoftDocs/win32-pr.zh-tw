---
description: 重新命名在物件路徑中指定 (或目錄) 的裝置檔案。
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111253"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="a9782-103">CIM DeviceFile 類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="a9782-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="a9782-104">**重新命名** 方法會將裝置檔案重新命名 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="a9782-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="a9782-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="a9782-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="a9782-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="a9782-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9782-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a9782-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9782-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a9782-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9782-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a9782-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a9782-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a9782-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9782-111">語法</span><span class="sxs-lookup"><span data-stu-id="a9782-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="a9782-112">參數</span><span class="sxs-lookup"><span data-stu-id="a9782-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9782-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9782-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9782-114">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="a9782-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="a9782-115">範例： "c： \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="a9782-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9782-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9782-116">Return value</span></span>

<span data-ttu-id="a9782-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a9782-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a9782-118">**0**</span><span class="sxs-lookup"><span data-stu-id="a9782-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-119">成功。</span><span class="sxs-lookup"><span data-stu-id="a9782-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-120">**2**</span><span class="sxs-lookup"><span data-stu-id="a9782-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a9782-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-122">**8**</span><span class="sxs-lookup"><span data-stu-id="a9782-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-123">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="a9782-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-124">**9**</span><span class="sxs-lookup"><span data-stu-id="a9782-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-125">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="a9782-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-126">**10**</span><span class="sxs-lookup"><span data-stu-id="a9782-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-127">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="a9782-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-128">**11**</span><span class="sxs-lookup"><span data-stu-id="a9782-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-129">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="a9782-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-130">**12**</span><span class="sxs-lookup"><span data-stu-id="a9782-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-131">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="a9782-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-132">**13**</span><span class="sxs-lookup"><span data-stu-id="a9782-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-133">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="a9782-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-134">**14**</span><span class="sxs-lookup"><span data-stu-id="a9782-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-135">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="a9782-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-136">**15**</span><span class="sxs-lookup"><span data-stu-id="a9782-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-137">共用違規。</span><span class="sxs-lookup"><span data-stu-id="a9782-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-138">**16**</span><span class="sxs-lookup"><span data-stu-id="a9782-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-139">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="a9782-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-140">**17**</span><span class="sxs-lookup"><span data-stu-id="a9782-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-141">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="a9782-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="a9782-142">**21**</span><span class="sxs-lookup"><span data-stu-id="a9782-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a9782-143">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="a9782-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9782-144">備註</span><span class="sxs-lookup"><span data-stu-id="a9782-144">Remarks</span></span>

<span data-ttu-id="a9782-145">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a9782-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a9782-146">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a9782-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a9782-147">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a9782-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9782-148">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a9782-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9782-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9782-149">Requirements</span></span>



| <span data-ttu-id="a9782-150">需求</span><span class="sxs-lookup"><span data-stu-id="a9782-150">Requirement</span></span> | <span data-ttu-id="a9782-151">值</span><span class="sxs-lookup"><span data-stu-id="a9782-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9782-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9782-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a9782-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9782-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9782-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9782-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a9782-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9782-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9782-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="a9782-156">Namespace</span></span><br/>                | <span data-ttu-id="a9782-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a9782-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9782-158">MOF</span><span class="sxs-lookup"><span data-stu-id="a9782-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9782-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9782-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9782-160">DLL</span><span class="sxs-lookup"><span data-stu-id="a9782-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9782-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9782-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9782-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9782-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9782-163">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="a9782-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="a9782-164">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="a9782-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

