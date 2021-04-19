---
description: 終止 IME 共用。
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: EndIMEShare 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992546"
---
# <a name="endimeshare-function"></a><span data-ttu-id="e72b4-103">EndIMEShare 函式</span><span class="sxs-lookup"><span data-stu-id="e72b4-103">EndIMEShare function</span></span>

<span data-ttu-id="e72b4-104">終止 IME 共用。</span><span class="sxs-lookup"><span data-stu-id="e72b4-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="e72b4-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="e72b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="e72b4-106">Parameters</span></span>

<span data-ttu-id="e72b4-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e72b4-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e72b4-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e72b4-108">Return value</span></span>

<span data-ttu-id="e72b4-109">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e72b4-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="e72b4-110">Remarks</span></span>

<span data-ttu-id="e72b4-111">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="e72b4-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="e72b4-112">呼叫最後一個 IME 共用函式之後，應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="e72b4-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e72b4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e72b4-113">Requirements</span></span>



| <span data-ttu-id="e72b4-114">需求</span><span class="sxs-lookup"><span data-stu-id="e72b4-114">Requirement</span></span> | <span data-ttu-id="e72b4-115">值</span><span class="sxs-lookup"><span data-stu-id="e72b4-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e72b4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e72b4-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e72b4-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e72b4-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e72b4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e72b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72b4-119">**FInitIMEShare**</span><span class="sxs-lookup"><span data-stu-id="e72b4-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
