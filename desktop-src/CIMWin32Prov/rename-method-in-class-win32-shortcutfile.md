---
description: 重新命名在物件路徑中指定的快捷方式檔案 (或目錄) 。
ms.assetid: 6325fe96-19ee-4ccc-934c-ef0c0668f353
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的重新命名方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c095a702269084a938887ef9717253df4653aea0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973560"
---
# <a name="rename-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="124b7-103">Win32 ShortcutFile 類別的重新命名方法 \_</span><span class="sxs-lookup"><span data-stu-id="124b7-103">Rename method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="124b7-104">**重新命名** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會重新命名 (或在物件路徑中指定的目錄) 的快捷方式檔案。</span><span class="sxs-lookup"><span data-stu-id="124b7-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="124b7-105">如果目的地是在另一個磁片磁碟機上，或需要覆寫現有的邏輯檔案，則不支援重新命名。</span><span class="sxs-lookup"><span data-stu-id="124b7-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="124b7-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="124b7-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="124b7-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="124b7-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="124b7-108">語法</span><span class="sxs-lookup"><span data-stu-id="124b7-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="124b7-109">參數</span><span class="sxs-lookup"><span data-stu-id="124b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124b7-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="124b7-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="124b7-111">檔案 (或目錄) 的完整新名稱。</span><span class="sxs-lookup"><span data-stu-id="124b7-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="124b7-112">範例： c： \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="124b7-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124b7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="124b7-113">Return value</span></span>

<span data-ttu-id="124b7-114">如果成功重新命名檔案，則傳回值為 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="124b7-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="124b7-115">**0**</span><span class="sxs-lookup"><span data-stu-id="124b7-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="124b7-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-117">**2**</span><span class="sxs-lookup"><span data-stu-id="124b7-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="124b7-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-119">**8**</span><span class="sxs-lookup"><span data-stu-id="124b7-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="124b7-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-121">**9**</span><span class="sxs-lookup"><span data-stu-id="124b7-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="124b7-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-123">**10**</span><span class="sxs-lookup"><span data-stu-id="124b7-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="124b7-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-125">**11**</span><span class="sxs-lookup"><span data-stu-id="124b7-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="124b7-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-127">**12**</span><span class="sxs-lookup"><span data-stu-id="124b7-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="124b7-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-129">**13**</span><span class="sxs-lookup"><span data-stu-id="124b7-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="124b7-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-131">**14**</span><span class="sxs-lookup"><span data-stu-id="124b7-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="124b7-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-133">**15**</span><span class="sxs-lookup"><span data-stu-id="124b7-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="124b7-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-135">**16**</span><span class="sxs-lookup"><span data-stu-id="124b7-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="124b7-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-137">**17**</span><span class="sxs-lookup"><span data-stu-id="124b7-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="124b7-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="124b7-139">**21**</span><span class="sxs-lookup"><span data-stu-id="124b7-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="124b7-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="124b7-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="124b7-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="124b7-141">Requirements</span></span>



| <span data-ttu-id="124b7-142">需求</span><span class="sxs-lookup"><span data-stu-id="124b7-142">Requirement</span></span> | <span data-ttu-id="124b7-143">值</span><span class="sxs-lookup"><span data-stu-id="124b7-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="124b7-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="124b7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="124b7-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="124b7-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="124b7-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="124b7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="124b7-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="124b7-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="124b7-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="124b7-148">Namespace</span></span><br/>                | <span data-ttu-id="124b7-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="124b7-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="124b7-150">MOF</span><span class="sxs-lookup"><span data-stu-id="124b7-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="124b7-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="124b7-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="124b7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="124b7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="124b7-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="124b7-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124b7-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="124b7-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="124b7-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="124b7-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="124b7-156">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="124b7-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

