---
description: BERGetInteger 函式會解碼 BER 編碼的整數。
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: 'BERGetInteger 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850911"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="9e78f-103">BERGetInteger 函式</span><span class="sxs-lookup"><span data-stu-id="9e78f-103">BERGetInteger function</span></span>

<span data-ttu-id="9e78f-104">**BERGetInteger** 函式會解碼 BER 編碼的整數。</span><span class="sxs-lookup"><span data-stu-id="9e78f-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e78f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e78f-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="9e78f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e78f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e78f-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="9e78f-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9e78f-108">已解碼之整數的指標。</span><span class="sxs-lookup"><span data-stu-id="9e78f-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="9e78f-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="9e78f-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9e78f-110">傳回值指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9e78f-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="9e78f-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="9e78f-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9e78f-112">傳回之標頭長度的指標。</span><span class="sxs-lookup"><span data-stu-id="9e78f-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="9e78f-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="9e78f-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9e78f-114">資料長度的指標。</span><span class="sxs-lookup"><span data-stu-id="9e78f-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="9e78f-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="9e78f-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="9e78f-116">指向下一個 BER 專案之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9e78f-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e78f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e78f-117">Return value</span></span>

<span data-ttu-id="9e78f-118">如果函式成功 (也就是，如果找到有效的 BER 編碼整數並轉換) ，則傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9e78f-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="9e78f-119">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9e78f-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e78f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e78f-120">Requirements</span></span>



| <span data-ttu-id="9e78f-121">需求</span><span class="sxs-lookup"><span data-stu-id="9e78f-121">Requirement</span></span> | <span data-ttu-id="9e78f-122">值</span><span class="sxs-lookup"><span data-stu-id="9e78f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e78f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e78f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9e78f-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e78f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9e78f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e78f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9e78f-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e78f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e78f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9e78f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e78f-128"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9e78f-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e78f-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="9e78f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9e78f-130"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e78f-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="9e78f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e78f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e78f-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e78f-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




