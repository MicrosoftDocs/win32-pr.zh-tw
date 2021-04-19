---
description: 抓取目前進程之動態卸載模組清單的大小與位置。
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979455"
---
# <a name="rtlgetunloadeventtraceex-function"></a><span data-ttu-id="9d326-103">RtlGetUnloadEventTraceEx 函式</span><span class="sxs-lookup"><span data-stu-id="9d326-103">RtlGetUnloadEventTraceEx function</span></span>

<span data-ttu-id="9d326-104">抓取目前進程之動態卸載模組清單的大小與位置。</span><span class="sxs-lookup"><span data-stu-id="9d326-104">Retrieves the size and location of the dynamically unloaded module list for the current process.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d326-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d326-105">Syntax</span></span>


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a><span data-ttu-id="9d326-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d326-107">*ElementSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d326-107">*ElementSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d326-108">變數的指標，其中包含清單中元素的大小。</span><span class="sxs-lookup"><span data-stu-id="9d326-108">A pointer to a variable that contains the size of an element in the list.</span></span>

</dd> <dt>

<span data-ttu-id="9d326-109">*ElementCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d326-109">*ElementCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d326-110">變數的指標，其中包含清單中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="9d326-110">A pointer to a variable that contains the number of elements in the list.</span></span>

</dd> <dt>

<span data-ttu-id="9d326-111">*EventTrace* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d326-111">*EventTrace* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d326-112">**RTL 卸載 \_ \_ 事件 \_ 追蹤** 結構的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="9d326-112">A pointer to an array of **RTL\_UNLOAD\_EVENT\_TRACE** structures.</span></span> <span data-ttu-id="9d326-113">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9d326-113">For more information, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d326-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d326-114">Return value</span></span>

<span data-ttu-id="9d326-115">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9d326-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d326-116">備註</span><span class="sxs-lookup"><span data-stu-id="9d326-116">Remarks</span></span>

<span data-ttu-id="9d326-117">載入器會將卸載的事件資訊儲存在可跨進程讀取的位置，方法是利用在所有進程的相同基底位址載入 Ntdll.dll 的事實。</span><span class="sxs-lookup"><span data-stu-id="9d326-117">The loader stores unloaded event information in locations that can be read across processes by taking advantage of the fact that Ntdll.dll is loaded at the same base address in all processes.</span></span> <span data-ttu-id="9d326-118">當偵錯工具需要查詢卸載的模組資訊時，它會呼叫此函式來判斷變數所在的位址，然後在這些位址上查詢目標進程中的虛擬記憶體，以讀取實際值。</span><span class="sxs-lookup"><span data-stu-id="9d326-118">When a debugger needs to query unloaded module information, it calls this function to determine the address at which the variables reside, then queries the virtual memory in the target process at those addresses to read the actual values.</span></span>

<span data-ttu-id="9d326-119">清單中的每個元素都定義如下。</span><span class="sxs-lookup"><span data-stu-id="9d326-119">Each element in the list is defined as follows.</span></span>

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

<span data-ttu-id="9d326-120">此函數沒有相關聯的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="9d326-120">This function has no associated header file.</span></span> <span data-ttu-id="9d326-121">相關聯的匯入程式庫（Ntdll.dll）可在 Windows 驅動程式套件 (WDK) 中取得。</span><span class="sxs-lookup"><span data-stu-id="9d326-121">The associated import library, Ntdll.lib, is available in the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="9d326-122">您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="9d326-122">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d326-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d326-123">Requirements</span></span>



| <span data-ttu-id="9d326-124">需求</span><span class="sxs-lookup"><span data-stu-id="9d326-124">Requirement</span></span> | <span data-ttu-id="9d326-125">值</span><span class="sxs-lookup"><span data-stu-id="9d326-125">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d326-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9d326-126">DLL</span></span><br/> | <dl> <span data-ttu-id="9d326-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d326-127"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
