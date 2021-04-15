---
description: 將物件路徑中指定的邏輯快速鍵檔或目錄複寫到輸入參數所指定的位置。
ms.assetid: 1c8e9eac-340b-4c37-a52e-6cfade47ccf6
ms.tgt_platform: multiple
title: Win32_ShortcutFile 類別的 Copy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 58de9d1b2a88a7fa02504f5eac91e9a55e286304
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468261"
---
# <a name="copy-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="2087c-103">Win32 ShortcutFile 類別的 Copy 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2087c-103">Copy method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="2087c-104">**複製** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將物件路徑中指定的邏輯快速鍵檔或目錄複寫到輸入參數所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="2087c-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical shortcut file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="2087c-105">如果需要覆寫現有的邏輯檔案，則不支援複製。</span><span class="sxs-lookup"><span data-stu-id="2087c-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="2087c-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2087c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2087c-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2087c-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2087c-108">語法</span><span class="sxs-lookup"><span data-stu-id="2087c-108">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="2087c-109">參數</span><span class="sxs-lookup"><span data-stu-id="2087c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2087c-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2087c-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2087c-111"> (或目錄) 之檔案複本的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="2087c-111">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="2087c-112">範例： c： \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="2087c-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2087c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2087c-113">Return value</span></span>

<span data-ttu-id="2087c-114">如果成功複製檔案，則傳回 0 (零) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="2087c-114">Returns value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2087c-115">**0**</span><span class="sxs-lookup"><span data-stu-id="2087c-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-116">要求成功。</span><span class="sxs-lookup"><span data-stu-id="2087c-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-117">**2**</span><span class="sxs-lookup"><span data-stu-id="2087c-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-118">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="2087c-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-119">**8**</span><span class="sxs-lookup"><span data-stu-id="2087c-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-120">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="2087c-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-121">**9**</span><span class="sxs-lookup"><span data-stu-id="2087c-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-122">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="2087c-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-123">**10**</span><span class="sxs-lookup"><span data-stu-id="2087c-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-124">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="2087c-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-125">**11**</span><span class="sxs-lookup"><span data-stu-id="2087c-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-126">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="2087c-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-127">**12**</span><span class="sxs-lookup"><span data-stu-id="2087c-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-128">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="2087c-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-129">**13**</span><span class="sxs-lookup"><span data-stu-id="2087c-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-130">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="2087c-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-131">**14**</span><span class="sxs-lookup"><span data-stu-id="2087c-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-132">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="2087c-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-133">**15**</span><span class="sxs-lookup"><span data-stu-id="2087c-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-134">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="2087c-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-135">**16**</span><span class="sxs-lookup"><span data-stu-id="2087c-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-136">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="2087c-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-137">**17**</span><span class="sxs-lookup"><span data-stu-id="2087c-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-138">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="2087c-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2087c-139">**21**</span><span class="sxs-lookup"><span data-stu-id="2087c-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2087c-140">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="2087c-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2087c-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="2087c-141">Requirements</span></span>



| <span data-ttu-id="2087c-142">需求</span><span class="sxs-lookup"><span data-stu-id="2087c-142">Requirement</span></span> | <span data-ttu-id="2087c-143">值</span><span class="sxs-lookup"><span data-stu-id="2087c-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2087c-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2087c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2087c-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2087c-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2087c-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2087c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2087c-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2087c-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2087c-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="2087c-148">Namespace</span></span><br/>                | <span data-ttu-id="2087c-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2087c-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2087c-150">MOF</span><span class="sxs-lookup"><span data-stu-id="2087c-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2087c-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2087c-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2087c-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2087c-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2087c-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2087c-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2087c-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2087c-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="2087c-155">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2087c-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2087c-156">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="2087c-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

