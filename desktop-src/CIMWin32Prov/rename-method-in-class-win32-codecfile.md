---
description: 重新命名物件路徑中指定的編解碼器檔案。
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4eb931a0155518ad9644ebb1cce0b604be80602
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936432"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a><span data-ttu-id="d0720-103">Win32 CodecFile 類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="d0720-103">Rename method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="d0720-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名物件路徑中指定的編解碼器檔案。</span><span class="sxs-lookup"><span data-stu-id="d0720-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the codec file specified in the object path.</span></span> <span data-ttu-id="d0720-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="d0720-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="d0720-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d0720-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d0720-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d0720-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0720-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0720-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d0720-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0720-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0720-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d0720-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d0720-111">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="d0720-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="d0720-112">範例： c： \\ temp \\newfile.txt。</span><span class="sxs-lookup"><span data-stu-id="d0720-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0720-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0720-113">Return value</span></span>

<span data-ttu-id="d0720-114">傳回整數值 0 (零) 如果成功重新命名檔案，則傳回任何其他數位，表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0720-114">Returns an integer value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d0720-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d0720-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="d0720-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-117">**2**</span><span class="sxs-lookup"><span data-stu-id="d0720-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="d0720-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-119">**8**</span><span class="sxs-lookup"><span data-stu-id="d0720-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="d0720-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-121">**9**</span><span class="sxs-lookup"><span data-stu-id="d0720-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="d0720-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-123">**10**</span><span class="sxs-lookup"><span data-stu-id="d0720-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="d0720-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-125">**11**</span><span class="sxs-lookup"><span data-stu-id="d0720-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="d0720-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-127">**12**</span><span class="sxs-lookup"><span data-stu-id="d0720-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="d0720-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-129">**13**</span><span class="sxs-lookup"><span data-stu-id="d0720-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="d0720-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-131">**14**</span><span class="sxs-lookup"><span data-stu-id="d0720-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="d0720-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-133">**15**</span><span class="sxs-lookup"><span data-stu-id="d0720-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="d0720-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-135">**16**</span><span class="sxs-lookup"><span data-stu-id="d0720-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="d0720-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-137">**17**</span><span class="sxs-lookup"><span data-stu-id="d0720-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="d0720-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d0720-139">**21**</span><span class="sxs-lookup"><span data-stu-id="d0720-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d0720-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d0720-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0720-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0720-141">Requirements</span></span>



| <span data-ttu-id="d0720-142">需求</span><span class="sxs-lookup"><span data-stu-id="d0720-142">Requirement</span></span> | <span data-ttu-id="d0720-143">值</span><span class="sxs-lookup"><span data-stu-id="d0720-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0720-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0720-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d0720-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0720-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0720-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0720-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d0720-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0720-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0720-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="d0720-148">Namespace</span></span><br/>                | <span data-ttu-id="d0720-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d0720-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0720-150">MOF</span><span class="sxs-lookup"><span data-stu-id="d0720-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0720-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0720-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0720-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d0720-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0720-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0720-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0720-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0720-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0720-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0720-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d0720-156">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="d0720-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

