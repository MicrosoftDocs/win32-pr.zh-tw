---
description: 抓取指定目錄物件的相關資訊。
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: NtQueryDirectoryObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000715"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="1133d-103">NtQueryDirectoryObject 函式</span><span class="sxs-lookup"><span data-stu-id="1133d-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="1133d-104">\[這項功能可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1133d-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1133d-105">抓取指定目錄物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1133d-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1133d-106">語法</span><span class="sxs-lookup"><span data-stu-id="1133d-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="1133d-107">參數</span><span class="sxs-lookup"><span data-stu-id="1133d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1133d-108">*DirectoryHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1133d-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-109">目錄物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1133d-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-110">*緩衝區* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="1133d-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-111">接收目錄資訊的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="1133d-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="1133d-112">這個緩衝區會接收一或多個 **物件 \_ 目錄 \_ 資訊** 結構，最後一個是 **Null**，後面接著包含目錄專案名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="1133d-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="1133d-113">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="1133d-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-114">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1133d-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-115">使用者提供的輸出緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1133d-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-116">*ReturnSingleEntry* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1133d-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-117">指出函數是否只傳回單一專案。</span><span class="sxs-lookup"><span data-stu-id="1133d-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-118">*RestartScan* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1133d-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-119">指出是否要使用 *內容* 參數中傳遞的資訊，重新開機掃描或繼續列舉。</span><span class="sxs-lookup"><span data-stu-id="1133d-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-120">*內容* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="1133d-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-121">列舉內容。</span><span class="sxs-lookup"><span data-stu-id="1133d-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="1133d-122">*ReturnLength* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="1133d-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1133d-123">變數的指標，此變數會接收輸出緩衝區中傳回之目錄資訊的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1133d-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1133d-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="1133d-124">Return value</span></span>

<span data-ttu-id="1133d-125">函數會傳回 **狀態 \_ 成功** 或錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="1133d-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="1133d-126">備註</span><span class="sxs-lookup"><span data-stu-id="1133d-126">Remarks</span></span>

<span data-ttu-id="1133d-127">以下是 **物件 \_ 目錄 \_ 資訊** 結構的定義。</span><span class="sxs-lookup"><span data-stu-id="1133d-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="1133d-128">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="1133d-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1133d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1133d-129">Requirements</span></span>



| <span data-ttu-id="1133d-130">需求</span><span class="sxs-lookup"><span data-stu-id="1133d-130">Requirement</span></span> | <span data-ttu-id="1133d-131">值</span><span class="sxs-lookup"><span data-stu-id="1133d-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1133d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1133d-132">DLL</span></span><br/> | <dl> <span data-ttu-id="1133d-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1133d-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1133d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1133d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1133d-135">**NtOpenDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="1133d-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
