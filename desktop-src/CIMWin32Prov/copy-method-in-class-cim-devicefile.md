---
description: CIM_DeviceFile 類別的 copy 方法-Copy 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: CIM_DeviceFile 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089797"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="38a77-103">CIM DeviceFile 類別的 Copy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="38a77-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="38a77-104">**Copy** 方法會將物件路徑中指定的邏輯檔案 (或目錄) 複製到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="38a77-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="38a77-105">如果需要覆寫現有的邏輯檔案，則不支援複本。</span><span class="sxs-lookup"><span data-stu-id="38a77-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="38a77-106">這個方法繼承自 [**CIM \_ LogicalFile**](cim-logicalfile.md)。</span><span class="sxs-lookup"><span data-stu-id="38a77-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38a77-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="38a77-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="38a77-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="38a77-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="38a77-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="38a77-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="38a77-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="38a77-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="38a77-111">語法</span><span class="sxs-lookup"><span data-stu-id="38a77-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="38a77-112">參數</span><span class="sxs-lookup"><span data-stu-id="38a77-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38a77-113">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38a77-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38a77-114">目的地檔案的完整名稱 (或目錄) 複製。</span><span class="sxs-lookup"><span data-stu-id="38a77-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="38a77-115">範例： "c： \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="38a77-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38a77-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="38a77-116">Return value</span></span>

<span data-ttu-id="38a77-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="38a77-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="38a77-118">**0**</span><span class="sxs-lookup"><span data-stu-id="38a77-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-119">成功。</span><span class="sxs-lookup"><span data-stu-id="38a77-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-120">**2**</span><span class="sxs-lookup"><span data-stu-id="38a77-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-121">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="38a77-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-122">**8**</span><span class="sxs-lookup"><span data-stu-id="38a77-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-123">未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="38a77-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-124">**9**</span><span class="sxs-lookup"><span data-stu-id="38a77-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-125">不正確物件。</span><span class="sxs-lookup"><span data-stu-id="38a77-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-126">**10**</span><span class="sxs-lookup"><span data-stu-id="38a77-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-127">物件已存在。</span><span class="sxs-lookup"><span data-stu-id="38a77-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-128">**11**</span><span class="sxs-lookup"><span data-stu-id="38a77-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-129">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="38a77-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-130">**12**</span><span class="sxs-lookup"><span data-stu-id="38a77-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-131">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="38a77-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-132">**13**</span><span class="sxs-lookup"><span data-stu-id="38a77-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-133">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="38a77-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-134">**14**</span><span class="sxs-lookup"><span data-stu-id="38a77-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-135">目錄未清空。</span><span class="sxs-lookup"><span data-stu-id="38a77-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-136">**15**</span><span class="sxs-lookup"><span data-stu-id="38a77-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-137">共用違規。</span><span class="sxs-lookup"><span data-stu-id="38a77-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-138">**16**</span><span class="sxs-lookup"><span data-stu-id="38a77-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-139">不正確啟動檔案。</span><span class="sxs-lookup"><span data-stu-id="38a77-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-140">**17**</span><span class="sxs-lookup"><span data-stu-id="38a77-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-141">未保留許可權。</span><span class="sxs-lookup"><span data-stu-id="38a77-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="38a77-142">**21**</span><span class="sxs-lookup"><span data-stu-id="38a77-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="38a77-143">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="38a77-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38a77-144">備註</span><span class="sxs-lookup"><span data-stu-id="38a77-144">Remarks</span></span>

<span data-ttu-id="38a77-145">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="38a77-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="38a77-146">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="38a77-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="38a77-147">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="38a77-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="38a77-148">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="38a77-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a77-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="38a77-149">Requirements</span></span>



| <span data-ttu-id="38a77-150">需求</span><span class="sxs-lookup"><span data-stu-id="38a77-150">Requirement</span></span> | <span data-ttu-id="38a77-151">值</span><span class="sxs-lookup"><span data-stu-id="38a77-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38a77-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38a77-152">Minimum supported client</span></span><br/> | <span data-ttu-id="38a77-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38a77-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38a77-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38a77-154">Minimum supported server</span></span><br/> | <span data-ttu-id="38a77-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38a77-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38a77-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="38a77-156">Namespace</span></span><br/>                | <span data-ttu-id="38a77-157">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="38a77-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38a77-158">MOF</span><span class="sxs-lookup"><span data-stu-id="38a77-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38a77-159"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="38a77-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38a77-160">DLL</span><span class="sxs-lookup"><span data-stu-id="38a77-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38a77-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38a77-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38a77-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38a77-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a77-163">CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="38a77-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="38a77-164">**CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="38a77-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

