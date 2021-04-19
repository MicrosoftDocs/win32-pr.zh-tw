---
description: 啟用傾印程式碼，從 Ntdll.dll 取得傾印中儲存的已卸載模組資訊。
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984794"
---
# <a name="rtlgetunloadeventtrace-function"></a><span data-ttu-id="6d050-103">RtlGetUnloadEventTrace 函式</span><span class="sxs-lookup"><span data-stu-id="6d050-103">RtlGetUnloadEventTrace function</span></span>

<span data-ttu-id="6d050-104">\[您可以在不另行通知的情況下，從 Windows 變更或移除此功能。\]</span><span class="sxs-lookup"><span data-stu-id="6d050-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="6d050-105">啟用傾印程式碼，從 Ntdll.dll 取得傾印中儲存的已卸載模組資訊。</span><span class="sxs-lookup"><span data-stu-id="6d050-105">Enables the dump code to get the unloaded module information from Ntdll.dll for storage in the minidump.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d050-106">語法</span><span class="sxs-lookup"><span data-stu-id="6d050-106">Syntax</span></span>


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="6d050-107">參數</span><span class="sxs-lookup"><span data-stu-id="6d050-107">Parameters</span></span>

<span data-ttu-id="6d050-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="6d050-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d050-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d050-109">Return value</span></span>

<span data-ttu-id="6d050-110">此函數會傳回陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="6d050-110">This function returns a pointer to an array.</span></span> <span data-ttu-id="6d050-111">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="6d050-111">For more information, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d050-112">備註</span><span class="sxs-lookup"><span data-stu-id="6d050-112">Remarks</span></span>

<span data-ttu-id="6d050-113">RtlpUnloadEventTrace 陣列的定義如下：</span><span class="sxs-lookup"><span data-stu-id="6d050-113">The RtlpUnloadEventTrace array is defined as follows:</span></span>

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

<span data-ttu-id="6d050-114">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="6d050-114">This function has no associated header file.</span></span> <span data-ttu-id="6d050-115">相關聯的匯入程式庫（Ntdll.dll）可在 Windows 驅動程式套件 (WDK) 中取得。</span><span class="sxs-lookup"><span data-stu-id="6d050-115">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="6d050-116">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="6d050-116">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d050-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d050-117">Requirements</span></span>



| <span data-ttu-id="6d050-118">需求</span><span class="sxs-lookup"><span data-stu-id="6d050-118">Requirement</span></span> | <span data-ttu-id="6d050-119">值</span><span class="sxs-lookup"><span data-stu-id="6d050-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6d050-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6d050-120">DLL</span></span><br/> | <dl> <span data-ttu-id="6d050-121"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d050-121"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
