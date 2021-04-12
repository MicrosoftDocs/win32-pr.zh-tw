---
description: 壓縮物件路徑中指定的邏輯編解碼器檔案 (或目錄) 。
ms.assetid: c53754cc-a220-428e-aaca-b7c27661f044
ms.tgt_platform: multiple
title: 壓縮 Win32_CodecFile 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f9eb201b1338dd4da9340519f88eab6c16c431
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187630"
---
# <a name="compress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="07337-103">壓縮 Win32 \_ CodecFile 類別的方法</span><span class="sxs-lookup"><span data-stu-id="07337-103">Compress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="07337-104">**壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將邏輯編解碼器檔案壓縮 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="07337-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="07337-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="07337-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07337-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="07337-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07337-107">語法</span><span class="sxs-lookup"><span data-stu-id="07337-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="07337-108">參數</span><span class="sxs-lookup"><span data-stu-id="07337-108">Parameters</span></span>

<span data-ttu-id="07337-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="07337-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07337-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="07337-110">Return value</span></span>

<span data-ttu-id="07337-111">傳回整數值 0 (零) 如果已成功壓縮檔案，則傳回任何其他數位，表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="07337-111">Returns an integer value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="07337-112">**0**</span><span class="sxs-lookup"><span data-stu-id="07337-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="07337-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="07337-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="07337-114">**2**</span><span class="sxs-lookup"><span data-stu-id="07337-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="07337-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="07337-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="07337-116">**8**</span><span class="sxs-lookup"><span data-stu-id="07337-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="07337-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="07337-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="07337-118">**9**</span><span class="sxs-lookup"><span data-stu-id="07337-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="07337-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="07337-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07337-120">**10**</span><span class="sxs-lookup"><span data-stu-id="07337-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="07337-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="07337-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="07337-122">**11**</span><span class="sxs-lookup"><span data-stu-id="07337-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="07337-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="07337-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="07337-124">**12**</span><span class="sxs-lookup"><span data-stu-id="07337-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="07337-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="07337-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="07337-126">**13**</span><span class="sxs-lookup"><span data-stu-id="07337-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="07337-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="07337-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="07337-128">**14**</span><span class="sxs-lookup"><span data-stu-id="07337-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="07337-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="07337-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="07337-130">**15**</span><span class="sxs-lookup"><span data-stu-id="07337-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="07337-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="07337-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="07337-132">**16**</span><span class="sxs-lookup"><span data-stu-id="07337-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="07337-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="07337-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="07337-134">**17**</span><span class="sxs-lookup"><span data-stu-id="07337-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="07337-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="07337-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="07337-136">**21**</span><span class="sxs-lookup"><span data-stu-id="07337-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="07337-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="07337-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07337-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="07337-138">Requirements</span></span>



| <span data-ttu-id="07337-139">需求</span><span class="sxs-lookup"><span data-stu-id="07337-139">Requirement</span></span> | <span data-ttu-id="07337-140">值</span><span class="sxs-lookup"><span data-stu-id="07337-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07337-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07337-141">Minimum supported client</span></span><br/> | <span data-ttu-id="07337-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07337-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07337-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07337-143">Minimum supported server</span></span><br/> | <span data-ttu-id="07337-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07337-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07337-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="07337-145">Namespace</span></span><br/>                | <span data-ttu-id="07337-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07337-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07337-147">MOF</span><span class="sxs-lookup"><span data-stu-id="07337-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07337-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="07337-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07337-149">DLL</span><span class="sxs-lookup"><span data-stu-id="07337-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07337-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07337-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07337-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07337-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="07337-152">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07337-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="07337-153">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="07337-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

