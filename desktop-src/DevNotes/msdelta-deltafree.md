---
description: 釋出指定的記憶體區塊。
title: DeltaFree 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990239"
---
# <a name="deltafree-function"></a><span data-ttu-id="06f2a-103">DeltaFree 函式</span><span class="sxs-lookup"><span data-stu-id="06f2a-103">DeltaFree function</span></span>

<span data-ttu-id="06f2a-104">釋出指定的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="06f2a-104">Frees the specified memory block.</span></span> <span data-ttu-id="06f2a-105">在成功呼叫 [CreateDeltaB](msdelta-createdeltab.md) 和 [ApplyDeltaB](msdelta-applydeltab.md) 之後，您必須呼叫此函式，以釋放 MSDelta 配置的記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="06f2a-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f2a-106">語法</span><span class="sxs-lookup"><span data-stu-id="06f2a-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="06f2a-107">參數</span><span class="sxs-lookup"><span data-stu-id="06f2a-107">Parameters</span></span>

<span data-ttu-id="06f2a-108">*lpMemory*</span><span class="sxs-lookup"><span data-stu-id="06f2a-108">*lpMemory*</span></span>

<span data-ttu-id="06f2a-109">在要釋放的記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="06f2a-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="06f2a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="06f2a-110">Return value</span></span>

<span data-ttu-id="06f2a-111">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="06f2a-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="06f2a-112">當函數傳回 **FALSE** 時，您可以呼叫 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得對應的 Win32 系統錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="06f2a-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06f2a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="06f2a-113">Requirements</span></span>

| <span data-ttu-id="06f2a-114">需求</span><span class="sxs-lookup"><span data-stu-id="06f2a-114">Requirement</span></span> | <span data-ttu-id="06f2a-115">值</span><span class="sxs-lookup"><span data-stu-id="06f2a-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06f2a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="06f2a-116">Header</span></span> | <span data-ttu-id="06f2a-117">msdelta。h</span><span class="sxs-lookup"><span data-stu-id="06f2a-117">msdelta.h</span></span> |
| <span data-ttu-id="06f2a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="06f2a-118">DLL</span></span> | <span data-ttu-id="06f2a-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="06f2a-119">msdelta.dll</span></span> |
| <span data-ttu-id="06f2a-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="06f2a-120">Unicode</span></span> | <span data-ttu-id="06f2a-121">不適用</span><span class="sxs-lookup"><span data-stu-id="06f2a-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="06f2a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06f2a-122">See also</span></span>

[<span data-ttu-id="06f2a-123">MSDelta</span><span class="sxs-lookup"><span data-stu-id="06f2a-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="06f2a-124">CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="06f2a-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="06f2a-125">ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="06f2a-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
