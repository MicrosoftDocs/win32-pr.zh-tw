---
description: 搜尋離線檔案快取中符合指定準則的檔案。
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: CSCFindFirstFileW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995025"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="7d6b2-103">CSCFindFirstFileW 函式</span><span class="sxs-lookup"><span data-stu-id="7d6b2-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="7d6b2-104">\[這項功能不受支援，因此不應該使用。\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="7d6b2-105">搜尋離線檔案快取中符合指定準則的檔案。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6b2-106">語法</span><span class="sxs-lookup"><span data-stu-id="7d6b2-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="7d6b2-107">參數</span><span class="sxs-lookup"><span data-stu-id="7d6b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6b2-108">*lpszFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-109">以 null 結束的字串指標，指定有效的 UNC 目錄或路徑。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="7d6b2-110">*lpFind32* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-111">[**WIN32 \_ 尋找 \_ 資料**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)結構的指標，此結構會接收檔案或子目錄的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="7d6b2-112">*lpdwStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-113">表示撥號狀態的 NTSTATUS 程式碼。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="7d6b2-114">*lpdwPinCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-115">如果檔案已離線提供，則此參數為非零，否則為0。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="7d6b2-116">*lpdwHintFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-117">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="7d6b2-118">值</span><span class="sxs-lookup"><span data-stu-id="7d6b2-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="7d6b2-119">意義</span><span class="sxs-lookup"><span data-stu-id="7d6b2-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="7d6b2-120"><dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 使用者**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b2-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="7d6b2-121">使用者使檔案可離線使用。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="7d6b2-122"><dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 繼承 \_ 使用者**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b2-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="7d6b2-123">使用者已讓父代可離線使用，並標示父系，使其子系可供離線使用。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="7d6b2-124"><dt>**旗 \_ 標CSC \_ 提示 \_ PIN \_ 繼承 \_ 系統**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b2-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="7d6b2-125">系統管理員或群組原則已讓父系可離線使用，並標示父系，使其子系可供離線使用。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="7d6b2-126"><dt>**旗 \_ 標CSC \_ 提示 \_ 針腳 \_ 系統**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b2-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="7d6b2-127">系統管理員或群組原則已讓檔案可離線使用。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="7d6b2-128">*lpOrgFileTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d6b2-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6b2-129">要接收檔案或子目錄之日期和時間資訊的 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6b2-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d6b2-130">Return value</span></span>

<span data-ttu-id="7d6b2-131">如果函式成功，則傳回值是在後續呼叫 [**CSCFindNextFileW**](cscfindnextfilew.md) 或 [**CSCFindClose**](cscfindclose.md)時所使用的搜尋控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="7d6b2-132">如果函式失敗，則傳回值是 **INVALID\_HANDLE\_VALUE**。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6b2-133">備註</span><span class="sxs-lookup"><span data-stu-id="7d6b2-133">Remarks</span></span>

<span data-ttu-id="7d6b2-134">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="7d6b2-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6b2-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d6b2-135">Requirements</span></span>



| <span data-ttu-id="7d6b2-136">需求</span><span class="sxs-lookup"><span data-stu-id="7d6b2-136">Requirement</span></span> | <span data-ttu-id="7d6b2-137">值</span><span class="sxs-lookup"><span data-stu-id="7d6b2-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6b2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7d6b2-138">DLL</span></span><br/> | <dl> <span data-ttu-id="7d6b2-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d6b2-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
