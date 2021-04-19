---
description: 完成使用 sprintf 樣式追蹤的選擇性欄位來設定追蹤緩衝區。
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978664"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="75c82-103">SetAsyncTraceParamsEx 函式</span><span class="sxs-lookup"><span data-stu-id="75c82-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="75c82-104">完成使用 **sprintf** 樣式追蹤的選擇性欄位來設定追蹤緩衝區。</span><span class="sxs-lookup"><span data-stu-id="75c82-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c82-105">語法</span><span class="sxs-lookup"><span data-stu-id="75c82-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="75c82-106">參數</span><span class="sxs-lookup"><span data-stu-id="75c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c82-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="75c82-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="75c82-108">與追蹤相關聯的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="75c82-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="75c82-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="75c82-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="75c82-110">包含例外狀況的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="75c82-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="75c82-111">*行*</span><span class="sxs-lookup"><span data-stu-id="75c82-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="75c82-112">來源檔案中例外狀況的行號。</span><span class="sxs-lookup"><span data-stu-id="75c82-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="75c82-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="75c82-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="75c82-114">例外狀況的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="75c82-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="75c82-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="75c82-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="75c82-116">追蹤旗標常數，表示其中一種可用的追蹤類型。</span><span class="sxs-lookup"><span data-stu-id="75c82-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="75c82-117">這個參數可以是下列任何一個值。</span><span class="sxs-lookup"><span data-stu-id="75c82-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="75c82-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**嚴重 \_追蹤 \_ 遮罩** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="75c82-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**錯誤 \_追蹤 \_ 遮罩** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="75c82-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG \_追蹤 \_ 遮罩** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="75c82-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**狀態 \_追蹤 \_ 遮罩** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="75c82-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_追蹤 \_ 遮罩** (0x00000010) </span><span class="sxs-lookup"><span data-stu-id="75c82-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**訊息 \_ (\_** 0x00000020) 的追蹤遮罩</span><span class="sxs-lookup"><span data-stu-id="75c82-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="75c82-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**全部 \_追蹤 \_ 遮罩** (0xffffffff) </span><span class="sxs-lookup"><span data-stu-id="75c82-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c82-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="75c82-125">Return value</span></span>

<span data-ttu-id="75c82-126">如果函式成功，則此函數會傳回 1;否則，它會傳回0。</span><span class="sxs-lookup"><span data-stu-id="75c82-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c82-127">備註</span><span class="sxs-lookup"><span data-stu-id="75c82-127">Remarks</span></span>

<span data-ttu-id="75c82-128">Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。</span><span class="sxs-lookup"><span data-stu-id="75c82-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="75c82-129">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="75c82-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c82-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="75c82-130">Requirements</span></span>



| <span data-ttu-id="75c82-131">需求</span><span class="sxs-lookup"><span data-stu-id="75c82-131">Requirement</span></span> | <span data-ttu-id="75c82-132">值</span><span class="sxs-lookup"><span data-stu-id="75c82-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75c82-133">DLL</span><span class="sxs-lookup"><span data-stu-id="75c82-133">DLL</span></span><br/> | <dl> <span data-ttu-id="75c82-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c82-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
