---
description: GetFrameRecognizeData 函數會傳回 RECOGNIZEDATA 結構的資料表。 其中每個結構都包含通訊協定識別碼，以及指向資料中指定之通訊協定開頭的位移。
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: 'GetFrameRecognizeData 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936623"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="8ca90-104">GetFrameRecognizeData 函式</span><span class="sxs-lookup"><span data-stu-id="8ca90-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="8ca90-105">**GetFrameRecognizeData** 函數會傳回 **RECOGNIZEDATA** 結構的資料表。</span><span class="sxs-lookup"><span data-stu-id="8ca90-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="8ca90-106">其中每個結構都包含通訊協定識別碼，以及指向資料中指定之通訊協定開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="8ca90-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca90-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ca90-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="8ca90-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ca90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca90-109">*hFrame* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ca90-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca90-110">框架的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ca90-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca90-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ca90-111">Return value</span></span>

<span data-ttu-id="8ca90-112">如果函式成功，則傳回值是 **RECOGNIZEDATATABLE** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8ca90-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="8ca90-113">如果函式不成功，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="8ca90-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca90-114">備註</span><span class="sxs-lookup"><span data-stu-id="8ca90-114">Remarks</span></span>

<span data-ttu-id="8ca90-115">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetFrameRecognizeData** 函數。</span><span class="sxs-lookup"><span data-stu-id="8ca90-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca90-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca90-116">Requirements</span></span>



| <span data-ttu-id="8ca90-117">需求</span><span class="sxs-lookup"><span data-stu-id="8ca90-117">Requirement</span></span> | <span data-ttu-id="8ca90-118">值</span><span class="sxs-lookup"><span data-stu-id="8ca90-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca90-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ca90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca90-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca90-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8ca90-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ca90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca90-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca90-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ca90-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8ca90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca90-124"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="8ca90-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8ca90-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ca90-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ca90-126"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ca90-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ca90-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca90-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca90-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca90-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




