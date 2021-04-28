---
description: AsyncStringTrace 函式-完成使用 sprintf 樣式追蹤的選擇性欄位來設定追蹤緩衝區。
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085796"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="c50d2-103">AsyncStringTrace 函式</span><span class="sxs-lookup"><span data-stu-id="c50d2-103">AsyncStringTrace function</span></span>

<span data-ttu-id="c50d2-104">完成使用 **sprintf** 樣式追蹤的選擇性欄位來設定追蹤緩衝區。</span><span class="sxs-lookup"><span data-stu-id="c50d2-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c50d2-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="c50d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c50d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50d2-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c50d2-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d2-108">用於應用層級篩選的32位追蹤參數。</span><span class="sxs-lookup"><span data-stu-id="c50d2-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="c50d2-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="c50d2-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d2-110">描述追蹤格式的以零結尾的字串。</span><span class="sxs-lookup"><span data-stu-id="c50d2-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="c50d2-111">*標記*</span><span class="sxs-lookup"><span data-stu-id="c50d2-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="c50d2-112">**Vsprintf** 函式的標記。</span><span class="sxs-lookup"><span data-stu-id="c50d2-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50d2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c50d2-113">Return value</span></span>

<span data-ttu-id="c50d2-114">此函數會傳回 trace 語句的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="c50d2-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50d2-115">備註</span><span class="sxs-lookup"><span data-stu-id="c50d2-115">Remarks</span></span>

<span data-ttu-id="c50d2-116">Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。</span><span class="sxs-lookup"><span data-stu-id="c50d2-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="c50d2-117">**Va \_ 清單** 資料類型是一種標準類型，可用來保存 **va \_ arg** 和 **va \_ end** 宏所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="c50d2-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="c50d2-118">如需詳細資訊，請參閱 [標準類型](/cpp/c-runtime-library/standard-types?view=vs-2019)。</span><span class="sxs-lookup"><span data-stu-id="c50d2-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="c50d2-119">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c50d2-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c50d2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c50d2-120">Requirements</span></span>



| <span data-ttu-id="c50d2-121">需求</span><span class="sxs-lookup"><span data-stu-id="c50d2-121">Requirement</span></span> | <span data-ttu-id="c50d2-122">值</span><span class="sxs-lookup"><span data-stu-id="c50d2-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c50d2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c50d2-123">DLL</span></span><br/> | <dl> <span data-ttu-id="c50d2-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50d2-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

