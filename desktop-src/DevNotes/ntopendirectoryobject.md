---
description: 開啟現有的目錄物件。
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995643"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="611f7-103">NtOpenDirectoryObject 函式</span><span class="sxs-lookup"><span data-stu-id="611f7-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="611f7-104">\[這項功能可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="611f7-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="611f7-105">開啟現有的目錄物件。</span><span class="sxs-lookup"><span data-stu-id="611f7-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="611f7-106">語法</span><span class="sxs-lookup"><span data-stu-id="611f7-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="611f7-107">參數</span><span class="sxs-lookup"><span data-stu-id="611f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="611f7-108">*DirectoryHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="611f7-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="611f7-109">新開啟的目錄物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="611f7-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="611f7-110">*DesiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="611f7-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611f7-111">[**存取 \_ 遮罩**](../secauthz/access-mask.md)，指定要求的目錄物件存取權。</span><span class="sxs-lookup"><span data-stu-id="611f7-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="611f7-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="611f7-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="611f7-113">值</span><span class="sxs-lookup"><span data-stu-id="611f7-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="611f7-114">意義</span><span class="sxs-lookup"><span data-stu-id="611f7-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="611f7-115"><dt>**目錄 \_查詢**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="611f7-116">查詢目錄物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="611f7-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="611f7-117"><dt>**目錄 \_遍歷**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="611f7-118">目錄物件的名稱查閱存取。</span><span class="sxs-lookup"><span data-stu-id="611f7-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="611f7-119"><dt>**目錄 \_建立 \_ 物件**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="611f7-120">目錄物件的名稱建立存取權。</span><span class="sxs-lookup"><span data-stu-id="611f7-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="611f7-121"><dt>**目錄 \_建立 \_ 子目錄**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="611f7-122">目錄物件的子目錄建立存取權。</span><span class="sxs-lookup"><span data-stu-id="611f7-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="611f7-123"><dt>**目錄 \_需要所有 \_ 存取**</dt><dt>標準 \_ 許可權 \_ \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="611f7-124">上述擁有權限加上 **\_ \_ 所需的標準許可權**。</span><span class="sxs-lookup"><span data-stu-id="611f7-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="611f7-125">*ObjectAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="611f7-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="611f7-126">目錄物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="611f7-126">The attributes for the directory object.</span></span> <span data-ttu-id="611f7-127">若要初始化 **物件 \_ 屬性** 結構，請使用 **InitializeObjectAttributes** 宏。</span><span class="sxs-lookup"><span data-stu-id="611f7-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="611f7-128">如需詳細資訊，請參閱 WDK 檔中的這些專案的說明文件。</span><span class="sxs-lookup"><span data-stu-id="611f7-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="611f7-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="611f7-129">Return value</span></span>

<span data-ttu-id="611f7-130">函數會傳回狀態 \_ 成功或錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="611f7-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="611f7-131">可能的狀態碼包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="611f7-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="611f7-132">傳回碼</span><span class="sxs-lookup"><span data-stu-id="611f7-132">Return code</span></span>                                                                                                       | <span data-ttu-id="611f7-133">Description</span><span class="sxs-lookup"><span data-stu-id="611f7-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="611f7-134"><dt>**狀態 \_ 不足的 \_ 資源**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="611f7-135">無法配置此函數所需的暫存緩衝區。</span><span class="sxs-lookup"><span data-stu-id="611f7-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="611f7-136"><dt>**狀態 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="611f7-137">指定的 ObjectAttributes 參數為 **Null** 指標，而不是 **物件 \_ 屬性** 結構的有效指標，或 **物件 \_ 屬性** 結構中指定的部分成員無效。</span><span class="sxs-lookup"><span data-stu-id="611f7-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="611f7-138"><dt>**狀態 \_ 物件 \_ 名稱 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="611f7-139">*ObjectAttributes* 參數包含 **物件 \_ 屬性** 結構中的 **ObjectName** 成員，因為在 **物件 \_ 名稱 \_ 路徑 \_ 分隔符號** 之後找到空字串，所以無效。</span><span class="sxs-lookup"><span data-stu-id="611f7-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="611f7-140"><dt>**\_ \_ \_ \_ 找不到狀態物件名稱**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="611f7-141">*ObjectAttributes* 參數包含 **物件 \_ 屬性** 結構中找不到的 **ObjectName** 成員。</span><span class="sxs-lookup"><span data-stu-id="611f7-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="611f7-142"><dt>**\_ \_ \_ \_ 找不到狀態物件路徑**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="611f7-143">*ObjectAttributes* 參數在 **物件 \_ 屬性** 結構中包含的 **ObjectName** 成員具有找不到的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="611f7-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="611f7-144"><dt>**狀態 \_物件 \_ 路徑 \_ 語法不 \_ 正確**</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="611f7-145">*ObjectAttributes* 參數未包含 **RootDirectory** 成員，但是 **物件 \_ 屬性** 結構中的 **ObjectName** 成員是空字串，或未包含 **物件 \_ 名稱 \_ 路徑 \_ 分隔符號**。</span><span class="sxs-lookup"><span data-stu-id="611f7-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="611f7-146">這表示物件路徑的語法不正確。</span><span class="sxs-lookup"><span data-stu-id="611f7-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="611f7-147">備註</span><span class="sxs-lookup"><span data-stu-id="611f7-147">Remarks</span></span>

<span data-ttu-id="611f7-148">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="611f7-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="611f7-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="611f7-149">Requirements</span></span>



| <span data-ttu-id="611f7-150">需求</span><span class="sxs-lookup"><span data-stu-id="611f7-150">Requirement</span></span> | <span data-ttu-id="611f7-151">值</span><span class="sxs-lookup"><span data-stu-id="611f7-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="611f7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="611f7-152">DLL</span></span><br/> | <dl> <span data-ttu-id="611f7-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="611f7-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611f7-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="611f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611f7-155">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="611f7-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
