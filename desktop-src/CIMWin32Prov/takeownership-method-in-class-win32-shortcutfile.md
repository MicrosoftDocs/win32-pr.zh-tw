---
description: TakeOwnerShip&\# 8194;WMI 類別方法會取得物件路徑中所指定之邏輯檔案的擁有權。
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 TakeOwnerShip 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5da7a237ae1943e65bc1cc757d5c4a16c6df8900
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936113"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="b6b07-103">Win32 ShortcutFile 類別的 TakeOwnerShip 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b6b07-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="b6b07-104">**TakeOwnerShip** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會取得物件路徑中所指定之邏輯檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="b6b07-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="b6b07-105">如果邏輯檔案實際上是目錄，則 **TakeOwnerShip** 會以遞迴方式運作，並取得目錄包含的所有檔案和子目錄的擁有權。</span><span class="sxs-lookup"><span data-stu-id="b6b07-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="b6b07-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="b6b07-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b6b07-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="b6b07-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b07-108">語法</span><span class="sxs-lookup"><span data-stu-id="b6b07-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="b6b07-109">參數</span><span class="sxs-lookup"><span data-stu-id="b6b07-109">Parameters</span></span>

<span data-ttu-id="b6b07-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b6b07-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6b07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6b07-111">Return value</span></span>

<span data-ttu-id="b6b07-112">傳回下列其中一個整數值。</span><span class="sxs-lookup"><span data-stu-id="b6b07-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="b6b07-113">**0**</span><span class="sxs-lookup"><span data-stu-id="b6b07-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-114">要求成功。</span><span class="sxs-lookup"><span data-stu-id="b6b07-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-115">**2**</span><span class="sxs-lookup"><span data-stu-id="b6b07-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-116">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="b6b07-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-117">**8**</span><span class="sxs-lookup"><span data-stu-id="b6b07-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-118">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="b6b07-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-119">**9**</span><span class="sxs-lookup"><span data-stu-id="b6b07-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-120">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="b6b07-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-121">**10**</span><span class="sxs-lookup"><span data-stu-id="b6b07-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-122">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="b6b07-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-123">**11**</span><span class="sxs-lookup"><span data-stu-id="b6b07-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-124">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="b6b07-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-125">**12**</span><span class="sxs-lookup"><span data-stu-id="b6b07-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-126">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="b6b07-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-127">**13**</span><span class="sxs-lookup"><span data-stu-id="b6b07-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-128">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="b6b07-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-129">**14**</span><span class="sxs-lookup"><span data-stu-id="b6b07-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-130">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="b6b07-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-131">**15**</span><span class="sxs-lookup"><span data-stu-id="b6b07-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-132">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="b6b07-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-133">**16**</span><span class="sxs-lookup"><span data-stu-id="b6b07-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-134">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="b6b07-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-135">**17**</span><span class="sxs-lookup"><span data-stu-id="b6b07-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-136">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="b6b07-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b6b07-137">**21**</span><span class="sxs-lookup"><span data-stu-id="b6b07-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b6b07-138">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="b6b07-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6b07-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6b07-139">Requirements</span></span>



| <span data-ttu-id="b6b07-140">需求</span><span class="sxs-lookup"><span data-stu-id="b6b07-140">Requirement</span></span> | <span data-ttu-id="b6b07-141">值</span><span class="sxs-lookup"><span data-stu-id="b6b07-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b07-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b6b07-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b07-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6b07-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6b07-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b6b07-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b07-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6b07-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6b07-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="b6b07-146">Namespace</span></span><br/>                | <span data-ttu-id="b6b07-147">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6b07-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6b07-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b6b07-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6b07-149"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6b07-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6b07-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b07-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b07-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6b07-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6b07-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6b07-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6b07-153">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6b07-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b6b07-154">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="b6b07-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

