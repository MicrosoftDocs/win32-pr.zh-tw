---
description: 傳回具有使用者或群組所持有之共用的存取權限的 uint32 點陣圖，而該共用會傳回該實例。
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Win32_Share 類別的 GetAccessMask 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936220"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="0d0ce-103">Win32 共用類別的 GetAccessMask 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0d0ce-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="0d0ce-104">**GetAccessMask** 方法會傳回具有使用者或群組（代表傳回實例）所持有之共用的存取權限的 uint32 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="0d0ce-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d0ce-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="0d0ce-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="0d0ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d0ce-108">Parameters</span></span>

<span data-ttu-id="0d0ce-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d0ce-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d0ce-110">Return value</span></span>

<span data-ttu-id="0d0ce-111">使用者或群組所持有之共用的存取權限。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="0d0ce-112">**檔案 \_ 清單 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-113">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-113">1 (0x1)</span></span>

<span data-ttu-id="0d0ce-114">授與從檔案讀取資料的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="0d0ce-115">若為目錄，此值會授與許可權來列出目錄的內容。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-116">**檔案 \_ 新增 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-117">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-117">2 (0x2)</span></span>

<span data-ttu-id="0d0ce-118">授與將資料寫入檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="0d0ce-119">若為目錄，此值會授與在目錄中建立檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-120">**檔案 \_ 新增 \_ 子目錄**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-121">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-121">4 (0x4)</span></span>

<span data-ttu-id="0d0ce-122">授與將資料附加至檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="0d0ce-123">若為目錄，此值會授與建立子目錄的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-124">**檔案 \_ 讀取 \_ EA**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-125">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-125">8 (0x8)</span></span>

<span data-ttu-id="0d0ce-126">授與讀取擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-127">**檔案 \_ 寫入 \_ EA**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-128">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-128">16 (0x10)</span></span>

<span data-ttu-id="0d0ce-129">授予寫入擴充屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-130">**檔案 \_ 遍歷**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-131">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-131">32 (0x20)</span></span>

<span data-ttu-id="0d0ce-132">授與許可權來執行檔案。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-132">Grants the right to execute a file.</span></span> <span data-ttu-id="0d0ce-133">若為目錄，可以進行目錄的往返。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-134">**檔案 \_ 刪除 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-135">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-135">64 (0x40)</span></span>

<span data-ttu-id="0d0ce-136">授與刪除目錄的許可權，以及它所包含的所有檔案 (其子) ，即使檔案是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-137">**檔案 \_ 讀取 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-138">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-138">128 (0x80)</span></span>

<span data-ttu-id="0d0ce-139">授與讀取檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-140">**檔案 \_ 寫入 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="0d0ce-141">256 (0x100)</span></span>

<span data-ttu-id="0d0ce-142">授與變更檔案屬性的許可權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-144">65536 (0x10000) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-144">65536 (0x10000)</span></span>

<span data-ttu-id="0d0ce-145">授與刪除存取權。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-146">**讀取 \_ 控制**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-147">131072 (0x20000) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-147">131072 (0x20000)</span></span>

<span data-ttu-id="0d0ce-148">授與安全描述項和擁有者的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-149">**寫入 \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-150">262144 (0x40000) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-150">262144 (0x40000)</span></span>

<span data-ttu-id="0d0ce-151">授與任意存取控制清單 (DACL) 的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-152">**寫入 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-153">524288 (0x80000) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-153">524288 (0x80000)</span></span>

<span data-ttu-id="0d0ce-154">指派寫入擁有者。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="0d0ce-155">**同步**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="0d0ce-156">1048576 (0x100000) </span><span class="sxs-lookup"><span data-stu-id="0d0ce-156">1048576 (0x100000)</span></span>

<span data-ttu-id="0d0ce-157">同步存取，並允許進程等候物件進入已發出信號的狀態。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d0ce-158">備註</span><span class="sxs-lookup"><span data-stu-id="0d0ce-158">Remarks</span></span>

<span data-ttu-id="0d0ce-159">**GetAccessMask** 方法是物件方法，並用於這個類別的出現位置。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="0d0ce-160">範例</span><span class="sxs-lookup"><span data-stu-id="0d0ce-160">Examples</span></span>

<span data-ttu-id="0d0ce-161">下列 VBScript 程式碼範例會建立共用資料夾，然後取得安全描述項中保護共用資料夾的存取遮罩值。</span><span class="sxs-lookup"><span data-stu-id="0d0ce-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="0d0ce-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d0ce-162">Requirements</span></span>



| <span data-ttu-id="0d0ce-163">需求</span><span class="sxs-lookup"><span data-stu-id="0d0ce-163">Requirement</span></span> | <span data-ttu-id="0d0ce-164">值</span><span class="sxs-lookup"><span data-stu-id="0d0ce-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0ce-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d0ce-165">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0ce-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d0ce-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d0ce-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d0ce-167">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0ce-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d0ce-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d0ce-169">命名空間</span><span class="sxs-lookup"><span data-stu-id="0d0ce-169">Namespace</span></span><br/>                | <span data-ttu-id="0d0ce-170">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d0ce-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d0ce-171">MOF</span><span class="sxs-lookup"><span data-stu-id="0d0ce-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d0ce-172"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d0ce-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d0ce-173">DLL</span><span class="sxs-lookup"><span data-stu-id="0d0ce-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d0ce-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d0ce-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0ce-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d0ce-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0ce-176">**Win32 \_ 共用**</span><span class="sxs-lookup"><span data-stu-id="0d0ce-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

