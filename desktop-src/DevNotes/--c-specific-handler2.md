---
description: 由編譯器呼叫以執行結構化例外狀況處理延伸模組。
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: '__C_specific_handler 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994647"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="408c2-103">\_\_C \_ 特定 \_ 處理常式函數</span><span class="sxs-lookup"><span data-stu-id="408c2-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="408c2-104">由編譯器呼叫以執行結構化例外狀況處理延伸模組。</span><span class="sxs-lookup"><span data-stu-id="408c2-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="408c2-105">\_每當設定 FLAGS UNW \_ 旗標 \_ EHANDLER 或 UNW \_ 旗標 \_ UHANDLER 時，就會在回溯資訊中出現語言特定處理常式的相對位址。</span><span class="sxs-lookup"><span data-stu-id="408c2-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="408c2-106">特定語言的處理常式會在搜尋例外狀況處理常式時呼叫，或做為回溯的一部分來呼叫。</span><span class="sxs-lookup"><span data-stu-id="408c2-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="408c2-107">如需詳細資訊，請參閱 [語言特定處理常式](/cpp/build/language-specific-handler)。</span><span class="sxs-lookup"><span data-stu-id="408c2-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="408c2-108">語法</span><span class="sxs-lookup"><span data-stu-id="408c2-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="408c2-109">參數</span><span class="sxs-lookup"><span data-stu-id="408c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408c2-110">*ExceptionRecord* \[在\]</span><span class="sxs-lookup"><span data-stu-id="408c2-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408c2-111">提供包含標準 Win64 定義之例外狀況記錄的指標。</span><span class="sxs-lookup"><span data-stu-id="408c2-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="408c2-112">*EstablisherFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="408c2-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408c2-113">此函式之固定堆疊配置的基底位址。</span><span class="sxs-lookup"><span data-stu-id="408c2-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="408c2-114">*CoNtextRecord* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="408c2-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="408c2-115">指向例外狀況引發時的例外狀況內容 (在例外狀況處理常式案例中) 或終止處理常式案例中 (目前的「回溯」內容) 。</span><span class="sxs-lookup"><span data-stu-id="408c2-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="408c2-116">*DispatcherCoNtext* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="408c2-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="408c2-117">指向此函數的發送器內容。</span><span class="sxs-lookup"><span data-stu-id="408c2-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="408c2-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="408c2-118">Requirements</span></span>



| <span data-ttu-id="408c2-119">需求</span><span class="sxs-lookup"><span data-stu-id="408c2-119">Requirement</span></span> | <span data-ttu-id="408c2-120">值</span><span class="sxs-lookup"><span data-stu-id="408c2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="408c2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="408c2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="408c2-122"><dt>Wdm</dt></span><span class="sxs-lookup"><span data-stu-id="408c2-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="408c2-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="408c2-123">Library</span></span><br/> | <dl> <span data-ttu-id="408c2-124"><dt>Ntoskrnl.exe .lib</dt></span><span class="sxs-lookup"><span data-stu-id="408c2-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="408c2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="408c2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="408c2-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="408c2-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

