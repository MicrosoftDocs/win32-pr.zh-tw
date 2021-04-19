---
description: 抓取符號連結的目標。
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994627"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="5b0e9-103">NtQuerySymbolicLinkObject 函式</span><span class="sxs-lookup"><span data-stu-id="5b0e9-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="5b0e9-104">\[這項功能可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5b0e9-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="5b0e9-105">抓取符號連結的目標。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0e9-106">語法</span><span class="sxs-lookup"><span data-stu-id="5b0e9-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="5b0e9-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b0e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0e9-108">*LinkHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b0e9-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0e9-109">符號連結物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="5b0e9-110">*LinkTarget* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5b0e9-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0e9-111">已初始化的 Unicode 字串指標，該字串會接收符號連結的目標。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="5b0e9-112">如果呼叫失敗，就必須設定 **MaximumLength** 和 **Buffer** 成員。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="5b0e9-113">*ReturnedLength* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="5b0e9-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b0e9-114">變數的指標，此變數會接收 *LinkTarget* 參數中所傳回之 Unicode 字串的長度。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="5b0e9-115">如果函數傳回的 **狀態 \_ 緩衝區 \_ 太 \_ 小**，此變數會接收所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0e9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b0e9-116">Return value</span></span>

<span data-ttu-id="5b0e9-117">函數會傳回 **狀態 \_ 成功** 或錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0e9-118">備註</span><span class="sxs-lookup"><span data-stu-id="5b0e9-118">Remarks</span></span>

<span data-ttu-id="5b0e9-119">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5b0e9-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0e9-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b0e9-120">Requirements</span></span>



| <span data-ttu-id="5b0e9-121">需求</span><span class="sxs-lookup"><span data-stu-id="5b0e9-121">Requirement</span></span> | <span data-ttu-id="5b0e9-122">值</span><span class="sxs-lookup"><span data-stu-id="5b0e9-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0e9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5b0e9-123">DLL</span></span><br/> | <dl> <span data-ttu-id="5b0e9-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0e9-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b0e9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b0e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0e9-126">**NtOpenSymbolicLinkObject**</span><span class="sxs-lookup"><span data-stu-id="5b0e9-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
