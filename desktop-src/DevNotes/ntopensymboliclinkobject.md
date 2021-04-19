---
description: 開啟現有的符號連結。
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: NtOpenSymbolicLinkObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994742"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="59948-103">NtOpenSymbolicLinkObject 函式</span><span class="sxs-lookup"><span data-stu-id="59948-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="59948-104">\[這項功能可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="59948-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="59948-105">開啟現有的符號連結。</span><span class="sxs-lookup"><span data-stu-id="59948-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="59948-106">語法</span><span class="sxs-lookup"><span data-stu-id="59948-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="59948-107">參數</span><span class="sxs-lookup"><span data-stu-id="59948-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59948-108">*LinkHandle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="59948-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59948-109">新開啟的符號連結物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="59948-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="59948-110">*DesiredAccess* \[在\]</span><span class="sxs-lookup"><span data-stu-id="59948-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59948-111">[**存取 \_ 遮罩**](../secauthz/access-mask.md)，指定要求的目錄物件存取權。</span><span class="sxs-lookup"><span data-stu-id="59948-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="59948-112">一般會使用一般讀取， \_ 以便將控制碼傳遞至 [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="59948-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="59948-113">*ObjectAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="59948-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59948-114">目錄物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="59948-114">The attributes for the directory object.</span></span> <span data-ttu-id="59948-115">若要初始化 **物件 \_ 屬性** 結構，請使用 **InitializeObjectAttributes** 宏。</span><span class="sxs-lookup"><span data-stu-id="59948-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="59948-116">如果呼叫端不是在系統執行緒內容中執行，它必須在初始化結構時指定 **OBJ \_ 核心 \_ 控制碼** 旗標。</span><span class="sxs-lookup"><span data-stu-id="59948-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="59948-117">如需詳細資訊，請參閱 WDK 檔中的這些專案的說明文件。</span><span class="sxs-lookup"><span data-stu-id="59948-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59948-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="59948-118">Return value</span></span>

<span data-ttu-id="59948-119">函數會傳回 **狀態 \_ 成功** 或錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="59948-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="59948-120">備註</span><span class="sxs-lookup"><span data-stu-id="59948-120">Remarks</span></span>

<span data-ttu-id="59948-121">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="59948-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="59948-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="59948-122">Requirements</span></span>



| <span data-ttu-id="59948-123">需求</span><span class="sxs-lookup"><span data-stu-id="59948-123">Requirement</span></span> | <span data-ttu-id="59948-124">值</span><span class="sxs-lookup"><span data-stu-id="59948-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59948-125">DLL</span><span class="sxs-lookup"><span data-stu-id="59948-125">DLL</span></span><br/> | <dl> <span data-ttu-id="59948-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59948-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59948-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59948-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59948-128">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="59948-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
