---
description: VarLenSmallIntToDword 函式會將可變長度的小整數轉換成 DWORD。
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: 'VarLenSmallIntToDword 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974404"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="93e07-103">VarLenSmallIntToDword 函式</span><span class="sxs-lookup"><span data-stu-id="93e07-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="93e07-104">**VarLenSmallIntToDword** 函式會將可變長度的小整數轉換成 **DWORD**。</span><span class="sxs-lookup"><span data-stu-id="93e07-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="93e07-105">語法</span><span class="sxs-lookup"><span data-stu-id="93e07-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="93e07-106">參數</span><span class="sxs-lookup"><span data-stu-id="93e07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93e07-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="93e07-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="93e07-108">變數長度、小整數的指標。</span><span class="sxs-lookup"><span data-stu-id="93e07-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="93e07-109">*ValueLen*</span><span class="sxs-lookup"><span data-stu-id="93e07-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="93e07-110">長度 (（以位元組為單位）) 可變長度、小整數。</span><span class="sxs-lookup"><span data-stu-id="93e07-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="93e07-111">*fIsByteswapped*</span><span class="sxs-lookup"><span data-stu-id="93e07-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="93e07-112">指出變數長度小整數是否為位元組交換的旗標。</span><span class="sxs-lookup"><span data-stu-id="93e07-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="93e07-113">*lpDword*</span><span class="sxs-lookup"><span data-stu-id="93e07-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="93e07-114">整數轉換成的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="93e07-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93e07-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="93e07-115">Return value</span></span>

<span data-ttu-id="93e07-116">傳回值是 **DWORD** 的指標。</span><span class="sxs-lookup"><span data-stu-id="93e07-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="93e07-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="93e07-117">Requirements</span></span>



| <span data-ttu-id="93e07-118">需求</span><span class="sxs-lookup"><span data-stu-id="93e07-118">Requirement</span></span> | <span data-ttu-id="93e07-119">值</span><span class="sxs-lookup"><span data-stu-id="93e07-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93e07-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93e07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="93e07-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e07-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="93e07-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93e07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="93e07-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93e07-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="93e07-124">標頭</span><span class="sxs-lookup"><span data-stu-id="93e07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="93e07-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="93e07-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="93e07-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="93e07-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="93e07-127"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="93e07-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="93e07-128">DLL</span><span class="sxs-lookup"><span data-stu-id="93e07-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93e07-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93e07-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




