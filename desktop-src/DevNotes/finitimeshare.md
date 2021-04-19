---
description: 初始化 IME 共用。
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: FInitIMEShare 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993421"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="338c4-103">FInitIMEShare 函式</span><span class="sxs-lookup"><span data-stu-id="338c4-103">FInitIMEShare function</span></span>

<span data-ttu-id="338c4-104">初始化 IME 共用。</span><span class="sxs-lookup"><span data-stu-id="338c4-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="338c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="338c4-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="338c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="338c4-106">Parameters</span></span>

<span data-ttu-id="338c4-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="338c4-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="338c4-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="338c4-108">Return value</span></span>

<span data-ttu-id="338c4-109">此函數會在成功時傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="338c4-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="338c4-110">備註</span><span class="sxs-lookup"><span data-stu-id="338c4-110">Remarks</span></span>

<span data-ttu-id="338c4-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="338c4-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="338c4-112">呼叫任何其他 IME 共用函式之前，應該先呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="338c4-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="338c4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="338c4-113">Requirements</span></span>



| <span data-ttu-id="338c4-114">需求</span><span class="sxs-lookup"><span data-stu-id="338c4-114">Requirement</span></span> | <span data-ttu-id="338c4-115">值</span><span class="sxs-lookup"><span data-stu-id="338c4-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="338c4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="338c4-116">DLL</span></span><br/> | <dl> <span data-ttu-id="338c4-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="338c4-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338c4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="338c4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338c4-119">**EndIMEShare**</span><span class="sxs-lookup"><span data-stu-id="338c4-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
