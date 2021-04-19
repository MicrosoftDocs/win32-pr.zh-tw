---
description: 將指定的離線登錄 hive 寫入檔案。
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: 'ORSaveHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992805"
---
# <a name="orsavehive-function"></a><span data-ttu-id="5850e-103">ORSaveHive 函式</span><span class="sxs-lookup"><span data-stu-id="5850e-103">ORSaveHive function</span></span>

<span data-ttu-id="5850e-104">將指定的離線登錄 hive 寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="5850e-104">Writes the specified offline registry hive to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5850e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5850e-105">Syntax</span></span>


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="5850e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5850e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5850e-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5850e-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5850e-108">離線登錄 hive 要儲存的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-108">A handle to the offline registry hive to save.</span></span>

</dd> <dt>

<span data-ttu-id="5850e-109">*lpHivePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5850e-109">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5850e-110">Unicode 字串的指標，指定登錄 hive 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5850e-110">A pointer to a Unicode string that specifies the name of the registry hive file.</span></span> <span data-ttu-id="5850e-111">這不可以是現有檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="5850e-111">This cannot be the name of an existing file.</span></span>

</dd> <dt>

<span data-ttu-id="5850e-112">*dwOsMajorVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5850e-112">*dwOsMajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5850e-113">作業系統的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-113">The major version number of the operating system.</span></span> <span data-ttu-id="5850e-114">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5850e-114">This member can be one of the following values.</span></span>



| <span data-ttu-id="5850e-115">值</span><span class="sxs-lookup"><span data-stu-id="5850e-115">Value</span></span>                                                                        | <span data-ttu-id="5850e-116">意義</span><span class="sxs-lookup"><span data-stu-id="5850e-116">Meaning</span></span>                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5850e-117"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-117"><dt>5</dt></span></span> </dl> | <span data-ttu-id="5850e-118">如果 *dwOsMinorVersion* 是1，則作業系統是 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="5850e-118">If *dwOsMinorVersion* is 1, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="5850e-119">如果 *dwOsMinorVersion* 為2，則作業系統為 windows Server 2003 R2、windows server 2003 或 Windows XP Professional x64 Edition。</span><span class="sxs-lookup"><span data-stu-id="5850e-119">If *dwOsMinorVersion* is 2, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span><br/> |
| <dl> <span data-ttu-id="5850e-120"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-120"><dt>6</dt></span></span> </dl> | <span data-ttu-id="5850e-121">如果 *dwOsMinorVersion* 為0，則作業系統是 windows Server 2008 或 windows Vista。</span><span class="sxs-lookup"><span data-stu-id="5850e-121">If *dwOsMinorVersion* is 0, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/> <span data-ttu-id="5850e-122">如果 *dwOsMinorVersion* 是1，則作業系統是 windows Server 2008 R2 或 windows 7。</span><span class="sxs-lookup"><span data-stu-id="5850e-122">If *dwOsMinorVersion* is 1, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="5850e-123">*dwOsMinorVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5850e-123">*dwOsMinorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5850e-124">作業系統的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-124">The minor version number of the operating system.</span></span> <span data-ttu-id="5850e-125">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5850e-125">This member can be one of the following values.</span></span>



| <span data-ttu-id="5850e-126">值</span><span class="sxs-lookup"><span data-stu-id="5850e-126">Value</span></span>                                                                        | <span data-ttu-id="5850e-127">意義</span><span class="sxs-lookup"><span data-stu-id="5850e-127">Meaning</span></span>                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5850e-128"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-128"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5850e-129">如果 *dwOsMajorVersion* 為6，則作業系統是 windows Server 2008 或 windows Vista。</span><span class="sxs-lookup"><span data-stu-id="5850e-129">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 or Windows Vista.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="5850e-130"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-130"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5850e-131">如果 *dwOsMajorVersion* 是5，則作業系統是 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="5850e-131">If *dwOsMajorVersion* is 5, the operating system is Windows XP.</span></span><br/> <span data-ttu-id="5850e-132">如果 *dwOsMajorVersion* 為6，則作業系統是 windows Server 2008 R2 或 windows 7。</span><span class="sxs-lookup"><span data-stu-id="5850e-132">If *dwOsMajorVersion* is 6, the operating system is Windows Server 2008 R2 or Windows 7.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="5850e-133"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-133"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5850e-134">如果 *dwOsMajorVersion* 是5，則作業系統是 windows Server 2003 R2、windows server 2003 或 Windows XP Professional x64 Edition。</span><span class="sxs-lookup"><span data-stu-id="5850e-134">If *dwOsMajorVersion* is 5, the operating system is Windows Server 2003 R2, Windows Server 2003, or Windows XP Professional x64 Edition.</span></span> <br/> <span data-ttu-id="5850e-135">如果 *dwOsMajorVersion* 為6， *dwOsMinorVersion* 參數必須是0或1。</span><span class="sxs-lookup"><span data-stu-id="5850e-135">If *dwOsMajorVersion* is 6, the *dwOsMinorVersion* parameter must be 0 or 1.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5850e-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="5850e-136">Return value</span></span>

<span data-ttu-id="5850e-137">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="5850e-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5850e-138">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="5850e-139">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="5850e-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="5850e-140">可能的錯誤代碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5850e-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="5850e-141">如果呼叫端沒有寫入檔案的必要存取權限，則函式會傳回 \_ 拒絕存取錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5850e-141">If the caller does not have the necessary access rights to write the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="5850e-142">如果指定的檔案已經存在，則函數會傳回 \_ 錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5850e-142">If the specified file already exists, the function returns ERROR\_ALREADY\_EXISTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="5850e-143">備註</span><span class="sxs-lookup"><span data-stu-id="5850e-143">Remarks</span></span>

<span data-ttu-id="5850e-144">您必須使用 **ORSaveHive** 函式來儲存對離線登錄 hive 進行的變更。</span><span class="sxs-lookup"><span data-stu-id="5850e-144">The **ORSaveHive** function must be used to save changes made to an offline registry hive.</span></span> <span data-ttu-id="5850e-145">在呼叫 **ORSaveHive** 將 hive 儲存至檔案之前，不會保留變更。</span><span class="sxs-lookup"><span data-stu-id="5850e-145">Changes are not preserved until **ORSaveHive** is called to save the hive to a file.</span></span>

<span data-ttu-id="5850e-146">*DwOsMajorVersion* 和 *dwOsMinorVersion* 參數會一起指定登錄 hive 檔案的目標格式。</span><span class="sxs-lookup"><span data-stu-id="5850e-146">The *dwOsMajorVersion* and *dwOsMinorVersion* parameters together specify the target format of the registry hive file.</span></span> <span data-ttu-id="5850e-147">下表摘要說明最新的作業系統版本號碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-147">The following table summarizes the most recent operating system version numbers.</span></span>



| <span data-ttu-id="5850e-148">作業系統</span><span class="sxs-lookup"><span data-stu-id="5850e-148">Operating system</span></span>                    | <span data-ttu-id="5850e-149">版本號碼</span><span class="sxs-lookup"><span data-stu-id="5850e-149">Version number</span></span> |
|-------------------------------------|----------------|
| <span data-ttu-id="5850e-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5850e-150">Windows Server 2008 R2</span></span>              | <span data-ttu-id="5850e-151">6.1</span><span class="sxs-lookup"><span data-stu-id="5850e-151">6.1</span></span>            |
| <span data-ttu-id="5850e-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5850e-152">Windows 7</span></span>                           | <span data-ttu-id="5850e-153">6.1</span><span class="sxs-lookup"><span data-stu-id="5850e-153">6.1</span></span>            |
| <span data-ttu-id="5850e-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5850e-154">Windows Server 2008</span></span>                 | <span data-ttu-id="5850e-155">6.0</span><span class="sxs-lookup"><span data-stu-id="5850e-155">6.0</span></span>            |
| <span data-ttu-id="5850e-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5850e-156">Windows Vista</span></span>                       | <span data-ttu-id="5850e-157">6.0</span><span class="sxs-lookup"><span data-stu-id="5850e-157">6.0</span></span>            |
| <span data-ttu-id="5850e-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5850e-158">Windows Server 2003 R2</span></span>              | <span data-ttu-id="5850e-159">5.2</span><span class="sxs-lookup"><span data-stu-id="5850e-159">5.2</span></span>            |
| <span data-ttu-id="5850e-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5850e-160">Windows Server 2003</span></span>                 | <span data-ttu-id="5850e-161">5.2</span><span class="sxs-lookup"><span data-stu-id="5850e-161">5.2</span></span>            |
| <span data-ttu-id="5850e-162">Windows XP Professional x64 Edition</span><span class="sxs-lookup"><span data-stu-id="5850e-162">Windows XP Professional x64 Edition</span></span> | <span data-ttu-id="5850e-163">5.2</span><span class="sxs-lookup"><span data-stu-id="5850e-163">5.2</span></span>            |
| <span data-ttu-id="5850e-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5850e-164">Windows XP</span></span>                          | <span data-ttu-id="5850e-165">5.1</span><span class="sxs-lookup"><span data-stu-id="5850e-165">5.1</span></span>            |



 

<span data-ttu-id="5850e-166">使用 [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) 函式取出目前作業系統的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5850e-166">Use the [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function to retrieve information about the current operating system.</span></span>

<span data-ttu-id="5850e-167">**ORSaveHive** 函式會在將 hive 寫入檔案時鎖定登錄 hive，然後關閉檔案並釋放鎖定。</span><span class="sxs-lookup"><span data-stu-id="5850e-167">The **ORSaveHive** function locks the registry hive while it is writing the hive to the file, then closes the file and releases the lock.</span></span> <span data-ttu-id="5850e-168">登錄 hive 會保留在記憶體中，直到透過呼叫 [**ORCloseHive**](orclosehive.md) 函式關閉為止。</span><span class="sxs-lookup"><span data-stu-id="5850e-168">The registry hive remains in memory until it is closed by calling the [**ORCloseHive**](orclosehive.md) function.</span></span> <span data-ttu-id="5850e-169">您可以在登錄 hive 開啟時進行進一步的變更;不過，若要保留這些變更，必須將 hive 儲存至新的檔案，因為 **ORSaveHive** 函式不會覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="5850e-169">It is possible to make further changes to the registry hive while it is open; however, to preserve these changes the hive must be saved to a new file, because the **ORSaveHive** function will not overwrite an existing file.</span></span>

<span data-ttu-id="5850e-170">**ORSaveHive** 函式可用於儲存離線登錄 hive 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5850e-170">The **ORSaveHive** function can be used to save part of the offline registry hive.</span></span> <span data-ttu-id="5850e-171">*控制碼* 參數中所指定的索引鍵會成為 hive 的根機碼，其中包含指定的索引鍵及其所有子機碼。</span><span class="sxs-lookup"><span data-stu-id="5850e-171">The key specified in the *Handle* parameter becomes the root key of a hive that consists of the specified key and all of its subkeys.</span></span>

## <a name="requirements"></a><span data-ttu-id="5850e-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="5850e-172">Requirements</span></span>



| <span data-ttu-id="5850e-173">需求</span><span class="sxs-lookup"><span data-stu-id="5850e-173">Requirement</span></span> | <span data-ttu-id="5850e-174">值</span><span class="sxs-lookup"><span data-stu-id="5850e-174">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5850e-175">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5850e-175">Redistributable</span></span><br/> | <span data-ttu-id="5850e-176">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="5850e-176">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="5850e-177">標頭</span><span class="sxs-lookup"><span data-stu-id="5850e-177">Header</span></span><br/>          | <dl> <span data-ttu-id="5850e-178"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-178"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5850e-179">DLL</span><span class="sxs-lookup"><span data-stu-id="5850e-179">DLL</span></span><br/>             | <dl> <span data-ttu-id="5850e-180"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5850e-180"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5850e-181">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5850e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5850e-182">GetVersionEx</span><span class="sxs-lookup"><span data-stu-id="5850e-182">GetVersionEx</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[<span data-ttu-id="5850e-183">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="5850e-183">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="5850e-184">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="5850e-184">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
