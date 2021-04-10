---
description: TakeOwnerShip WMI 類別方法會取得物件路徑中所指定之邏輯檔案的擁有權。
ms.assetid: c8fa0706-1f7e-4e68-aea6-694ba24c16c3
ms.tgt_platform: multiple
title: Win32_CodecFile 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1de05f444e99be9a1ebcb5d32fa0ba754cf34254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110172"
---
# <a name="takeownership-method-of-the-win32_codecfile-class"></a><span data-ttu-id="64304-103">Win32 CodecFile 類別的 TakeOwnerShip 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64304-103">TakeOwnerShip method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="64304-104">**TakeOwnerShip** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="64304-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="64304-105">如果邏輯檔案實際上是目錄，則 **TakeOwnerShip** 會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="64304-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="64304-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="64304-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="64304-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="64304-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="64304-108">語法</span><span class="sxs-lookup"><span data-stu-id="64304-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="64304-109">參數</span><span class="sxs-lookup"><span data-stu-id="64304-109">Parameters</span></span>

<span data-ttu-id="64304-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="64304-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64304-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="64304-111">Return value</span></span>

<span data-ttu-id="64304-112">傳回下列其中一個整數值。</span><span class="sxs-lookup"><span data-stu-id="64304-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="64304-113">**0**</span><span class="sxs-lookup"><span data-stu-id="64304-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="64304-114">要求成功。</span><span class="sxs-lookup"><span data-stu-id="64304-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="64304-115">**2**</span><span class="sxs-lookup"><span data-stu-id="64304-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="64304-116">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="64304-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="64304-117">**8**</span><span class="sxs-lookup"><span data-stu-id="64304-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="64304-118">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="64304-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="64304-119">**9**</span><span class="sxs-lookup"><span data-stu-id="64304-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="64304-120">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="64304-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="64304-121">**10**</span><span class="sxs-lookup"><span data-stu-id="64304-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="64304-122">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="64304-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="64304-123">**11**</span><span class="sxs-lookup"><span data-stu-id="64304-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="64304-124">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="64304-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="64304-125">**12**</span><span class="sxs-lookup"><span data-stu-id="64304-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="64304-126">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="64304-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="64304-127">**13**</span><span class="sxs-lookup"><span data-stu-id="64304-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="64304-128">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="64304-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="64304-129">**14**</span><span class="sxs-lookup"><span data-stu-id="64304-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="64304-130">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="64304-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="64304-131">**15**</span><span class="sxs-lookup"><span data-stu-id="64304-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="64304-132">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="64304-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="64304-133">**16**</span><span class="sxs-lookup"><span data-stu-id="64304-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="64304-134">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="64304-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="64304-135">**17**</span><span class="sxs-lookup"><span data-stu-id="64304-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="64304-136">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="64304-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="64304-137">**21**</span><span class="sxs-lookup"><span data-stu-id="64304-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="64304-138">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="64304-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64304-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="64304-139">Requirements</span></span>



| <span data-ttu-id="64304-140">需求</span><span class="sxs-lookup"><span data-stu-id="64304-140">Requirement</span></span> | <span data-ttu-id="64304-141">值</span><span class="sxs-lookup"><span data-stu-id="64304-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64304-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64304-142">Minimum supported client</span></span><br/> | <span data-ttu-id="64304-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64304-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64304-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64304-144">Minimum supported server</span></span><br/> | <span data-ttu-id="64304-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64304-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64304-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="64304-146">Namespace</span></span><br/>                | <span data-ttu-id="64304-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64304-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64304-148">MOF</span><span class="sxs-lookup"><span data-stu-id="64304-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64304-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="64304-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64304-150">DLL</span><span class="sxs-lookup"><span data-stu-id="64304-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64304-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64304-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64304-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64304-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="64304-153">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64304-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="64304-154">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="64304-154">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

