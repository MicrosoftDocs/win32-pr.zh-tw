---
description: Uncompresses 邏輯分頁檔案 (或在物件路徑中指定的目錄) 。
ms.assetid: 9bd98ba8-068e-49af-8dd4-e5ee987eb31d
ms.tgt_platform: multiple
title: Win32_PageFile 類別的解壓縮方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45a5b48ffa6b2249992b61eadf72f42f6d71969b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847535"
---
# <a name="uncompress-method-of-the-win32_pagefile-class"></a><span data-ttu-id="7abdf-103">Win32 \_ 分頁檔類別的解壓縮方法</span><span class="sxs-lookup"><span data-stu-id="7abdf-103">Uncompress method of the Win32\_PageFile class</span></span>

<span data-ttu-id="7abdf-104">[ **解壓縮** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class) ] 方法會 uncompresses 邏輯分頁檔案 (或在物件路徑中指定的目錄) 。</span><span class="sxs-lookup"><span data-stu-id="7abdf-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span>

<span data-ttu-id="7abdf-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="7abdf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7abdf-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="7abdf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7abdf-107">語法</span><span class="sxs-lookup"><span data-stu-id="7abdf-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="7abdf-108">參數</span><span class="sxs-lookup"><span data-stu-id="7abdf-108">Parameters</span></span>

<span data-ttu-id="7abdf-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7abdf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7abdf-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7abdf-110">Return value</span></span>

<span data-ttu-id="7abdf-111">如果檔案已成功解壓縮，則會傳回 0 (零) 的值，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="7abdf-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7abdf-112">**0**</span><span class="sxs-lookup"><span data-stu-id="7abdf-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-113">要求成功。</span><span class="sxs-lookup"><span data-stu-id="7abdf-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-114">**2**</span><span class="sxs-lookup"><span data-stu-id="7abdf-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-115">存取遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="7abdf-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-116">**8**</span><span class="sxs-lookup"><span data-stu-id="7abdf-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-117">發生未指定的失敗。</span><span class="sxs-lookup"><span data-stu-id="7abdf-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-118">**9**</span><span class="sxs-lookup"><span data-stu-id="7abdf-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-119">指定的名稱無效。</span><span class="sxs-lookup"><span data-stu-id="7abdf-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-120">**10**</span><span class="sxs-lookup"><span data-stu-id="7abdf-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-121">指定的物件已經存在。</span><span class="sxs-lookup"><span data-stu-id="7abdf-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-122">**11**</span><span class="sxs-lookup"><span data-stu-id="7abdf-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-123">檔案系統不是 NTFS。</span><span class="sxs-lookup"><span data-stu-id="7abdf-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-124">**12**</span><span class="sxs-lookup"><span data-stu-id="7abdf-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-125">平臺不是 Windows。</span><span class="sxs-lookup"><span data-stu-id="7abdf-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-126">**13**</span><span class="sxs-lookup"><span data-stu-id="7abdf-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-127">磁片磁碟機不相同。</span><span class="sxs-lookup"><span data-stu-id="7abdf-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-128">**14**</span><span class="sxs-lookup"><span data-stu-id="7abdf-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-129">目錄不是空的。</span><span class="sxs-lookup"><span data-stu-id="7abdf-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-130">**15**</span><span class="sxs-lookup"><span data-stu-id="7abdf-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-131">發生共用違規。</span><span class="sxs-lookup"><span data-stu-id="7abdf-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-132">**16**</span><span class="sxs-lookup"><span data-stu-id="7abdf-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-133">指定的起始檔無效。</span><span class="sxs-lookup"><span data-stu-id="7abdf-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-134">**17**</span><span class="sxs-lookup"><span data-stu-id="7abdf-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-135">不會保留操作所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="7abdf-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="7abdf-136">**21**</span><span class="sxs-lookup"><span data-stu-id="7abdf-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7abdf-137">指定的參數無效。</span><span class="sxs-lookup"><span data-stu-id="7abdf-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7abdf-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7abdf-138">Requirements</span></span>



| <span data-ttu-id="7abdf-139">需求</span><span class="sxs-lookup"><span data-stu-id="7abdf-139">Requirement</span></span> | <span data-ttu-id="7abdf-140">值</span><span class="sxs-lookup"><span data-stu-id="7abdf-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7abdf-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7abdf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7abdf-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7abdf-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7abdf-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7abdf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7abdf-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7abdf-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7abdf-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="7abdf-145">Namespace</span></span><br/>                | <span data-ttu-id="7abdf-146">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7abdf-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7abdf-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7abdf-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7abdf-148"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7abdf-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7abdf-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7abdf-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abdf-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7abdf-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7abdf-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7abdf-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="7abdf-152">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7abdf-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7abdf-153">**Win32 \_ 分頁檔**</span><span class="sxs-lookup"><span data-stu-id="7abdf-153">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

