---
description: Uncompresses 邏輯編解碼器檔案 (或在物件路徑中指定的目錄) 。
ms.assetid: abe74267-1274-4b20-82ac-51ca94d7af33
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的解壓縮方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d1ffcf99877781c7070b42dac5ffe9ef83af2d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847147"
---
# <a name="uncompress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="1d3c2-103">Win32 CodecFile 類別的解壓縮方法 \_</span><span class="sxs-lookup"><span data-stu-id="1d3c2-103">Uncompress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="1d3c2-104">[ **解壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class) ] 方法會 uncompresses 邏輯編解碼器檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="1d3c2-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d3c2-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d3c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="1d3c2-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="1d3c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="1d3c2-108">Parameters</span></span>

<span data-ttu-id="1d3c2-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d3c2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d3c2-110">Return value</span></span>

<span data-ttu-id="1d3c2-111">如果成功解壓縮檔案，則傳回整數值 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1d3c2-112">**0**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-114">**2**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-116">**8**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-118">**9**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-120">**10**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-122">**11**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-124">**12**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-126">**13**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-128">**14**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-130">**15**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-132">**16**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-134">**17**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1d3c2-136">**21**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1d3c2-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="1d3c2-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d3c2-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d3c2-138">Requirements</span></span>



| <span data-ttu-id="1d3c2-139">需求</span><span class="sxs-lookup"><span data-stu-id="1d3c2-139">Requirement</span></span> | <span data-ttu-id="1d3c2-140">值</span><span class="sxs-lookup"><span data-stu-id="1d3c2-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d3c2-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d3c2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1d3c2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d3c2-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d3c2-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d3c2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1d3c2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d3c2-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d3c2-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d3c2-145">Namespace</span></span><br/>                | <span data-ttu-id="1d3c2-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1d3c2-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d3c2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="1d3c2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d3c2-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d3c2-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d3c2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1d3c2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d3c2-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d3c2-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d3c2-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d3c2-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d3c2-152">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d3c2-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d3c2-153">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="1d3c2-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

