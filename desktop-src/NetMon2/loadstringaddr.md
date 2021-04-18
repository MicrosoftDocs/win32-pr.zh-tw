---
description: LoadStringAddr 函式會轉換字串 (例如 &\# 0034; 157.54.32.45&\# 0034; ) 並建立 DWORD 位址。
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: 'LoadStringAddr 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971247"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="cd02d-103">LoadStringAddr 函式</span><span class="sxs-lookup"><span data-stu-id="cd02d-103">LoadStringAddr function</span></span>

<span data-ttu-id="cd02d-104">**LoadStringAddr** 函式會轉換字串 (例如 "157.54.32.45" ) 並建立 **DWORD** 位址。</span><span class="sxs-lookup"><span data-stu-id="cd02d-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd02d-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd02d-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="cd02d-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd02d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd02d-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="cd02d-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="cd02d-108">**DWORD** 的指標。</span><span class="sxs-lookup"><span data-stu-id="cd02d-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="cd02d-109">*str*</span><span class="sxs-lookup"><span data-stu-id="cd02d-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="cd02d-110">字元字串的指標，其中包含 IP 位址的 x.x.x.x 表示 (例如 127.0.0.1) 。</span><span class="sxs-lookup"><span data-stu-id="cd02d-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd02d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd02d-111">Return value</span></span>

<span data-ttu-id="cd02d-112">如果函式成功 () 中找到位址名稱;傳回值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="cd02d-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="cd02d-113">如果函式不成功，則傳回值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cd02d-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd02d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd02d-114">Requirements</span></span>



| <span data-ttu-id="cd02d-115">需求</span><span class="sxs-lookup"><span data-stu-id="cd02d-115">Requirement</span></span> | <span data-ttu-id="cd02d-116">值</span><span class="sxs-lookup"><span data-stu-id="cd02d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd02d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd02d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd02d-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd02d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd02d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd02d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd02d-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd02d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd02d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cd02d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd02d-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="cd02d-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cd02d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd02d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd02d-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd02d-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd02d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd02d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd02d-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd02d-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




