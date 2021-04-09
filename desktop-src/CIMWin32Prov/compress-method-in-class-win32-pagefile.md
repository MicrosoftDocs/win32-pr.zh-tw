---
description: 壓縮物件路徑中指定 (或目錄) 的邏輯分頁檔。
ms.assetid: ebc69c9d-5a86-462b-9362-1ae02869ffa2
ms.tgt_platform: multiple
title: 壓縮 Win32_PageFile 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eabbe266356a5a5f4b0645b897bf36288b6174de
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847092"
---
# <a name="compress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="db8b0-103">壓縮 Win32 \_ 分頁檔類別的方法</span><span class="sxs-lookup"><span data-stu-id="db8b0-103">Compress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="db8b0-104">**壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將邏輯分頁檔案壓縮 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="db8b0-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="db8b0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="db8b0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db8b0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="db8b0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db8b0-107">語法</span><span class="sxs-lookup"><span data-stu-id="db8b0-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="db8b0-108">參數</span><span class="sxs-lookup"><span data-stu-id="db8b0-108">Parameters</span></span>

<span data-ttu-id="db8b0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="db8b0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db8b0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="db8b0-110">Return value</span></span>

<span data-ttu-id="db8b0-111">傳回值 0 (零) 如果檔案已成功壓縮，則為，而任何其他數位表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="db8b0-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="db8b0-112">**0**</span><span class="sxs-lookup"><span data-stu-id="db8b0-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="db8b0-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-114">**2**</span><span class="sxs-lookup"><span data-stu-id="db8b0-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="db8b0-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-116">**8**</span><span class="sxs-lookup"><span data-stu-id="db8b0-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="db8b0-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-118">**9**</span><span class="sxs-lookup"><span data-stu-id="db8b0-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="db8b0-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-120">**10**</span><span class="sxs-lookup"><span data-stu-id="db8b0-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="db8b0-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-122">**11**</span><span class="sxs-lookup"><span data-stu-id="db8b0-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="db8b0-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-124">**12**</span><span class="sxs-lookup"><span data-stu-id="db8b0-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="db8b0-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-126">**13**</span><span class="sxs-lookup"><span data-stu-id="db8b0-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="db8b0-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-128">**14**</span><span class="sxs-lookup"><span data-stu-id="db8b0-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="db8b0-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-130">**15**</span><span class="sxs-lookup"><span data-stu-id="db8b0-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="db8b0-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-132">**16**</span><span class="sxs-lookup"><span data-stu-id="db8b0-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="db8b0-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-134">**17**</span><span class="sxs-lookup"><span data-stu-id="db8b0-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="db8b0-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="db8b0-136">**21**</span><span class="sxs-lookup"><span data-stu-id="db8b0-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="db8b0-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="db8b0-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db8b0-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="db8b0-138">Requirements</span></span>



| <span data-ttu-id="db8b0-139">需求</span><span class="sxs-lookup"><span data-stu-id="db8b0-139">Requirement</span></span> | <span data-ttu-id="db8b0-140">值</span><span class="sxs-lookup"><span data-stu-id="db8b0-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db8b0-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db8b0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="db8b0-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db8b0-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db8b0-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db8b0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="db8b0-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db8b0-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db8b0-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="db8b0-145">Namespace</span></span><br/>                | <span data-ttu-id="db8b0-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db8b0-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db8b0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="db8b0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db8b0-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="db8b0-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db8b0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="db8b0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db8b0-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db8b0-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8b0-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db8b0-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="db8b0-152">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db8b0-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="db8b0-153">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="db8b0-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

