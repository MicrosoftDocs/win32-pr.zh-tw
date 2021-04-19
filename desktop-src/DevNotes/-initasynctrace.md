---
description: 初始化追蹤。
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: f79137fe4e832a193bafa59a573e5eb541884a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992830"
---
# <a name="initasynctrace-function"></a><span data-ttu-id="2fda0-103">InitAsyncTrace 函式</span><span class="sxs-lookup"><span data-stu-id="2fda0-103">InitAsyncTrace function</span></span>

<span data-ttu-id="2fda0-104">初始化追蹤。</span><span class="sxs-lookup"><span data-stu-id="2fda0-104">Initializes the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fda0-105">語法</span><span class="sxs-lookup"><span data-stu-id="2fda0-105">Syntax</span></span>


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="2fda0-106">參數</span><span class="sxs-lookup"><span data-stu-id="2fda0-106">Parameters</span></span>

<span data-ttu-id="2fda0-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="2fda0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fda0-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fda0-108">Return value</span></span>

<span data-ttu-id="2fda0-109">如果函式成功，則此函數會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="2fda0-109">This function returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fda0-110">備註</span><span class="sxs-lookup"><span data-stu-id="2fda0-110">Remarks</span></span>

<span data-ttu-id="2fda0-111">Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。</span><span class="sxs-lookup"><span data-stu-id="2fda0-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="2fda0-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="2fda0-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fda0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fda0-113">Requirements</span></span>



| <span data-ttu-id="2fda0-114">需求</span><span class="sxs-lookup"><span data-stu-id="2fda0-114">Requirement</span></span> | <span data-ttu-id="2fda0-115">值</span><span class="sxs-lookup"><span data-stu-id="2fda0-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fda0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2fda0-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2fda0-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fda0-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
