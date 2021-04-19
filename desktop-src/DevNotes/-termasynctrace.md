---
description: 結束追蹤。
ms.assetid: e823ed82-1966-4e44-b062-0c8ab0fb5f6e
title: TermAsyncTrace 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: c8f2ed58115130e141b5fc097965396847ebd147
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991170"
---
# <a name="termasynctrace-function"></a><span data-ttu-id="bbf94-103">TermAsyncTrace 函式</span><span class="sxs-lookup"><span data-stu-id="bbf94-103">TermAsyncTrace function</span></span>

<span data-ttu-id="bbf94-104">結束追蹤。</span><span class="sxs-lookup"><span data-stu-id="bbf94-104">Terminates the trace.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf94-105">語法</span><span class="sxs-lookup"><span data-stu-id="bbf94-105">Syntax</span></span>


```C++
BOOL TermAsyncTrace(void);
```



## <a name="parameters"></a><span data-ttu-id="bbf94-106">參數</span><span class="sxs-lookup"><span data-stu-id="bbf94-106">Parameters</span></span>

<span data-ttu-id="bbf94-107">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="bbf94-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbf94-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbf94-108">Return value</span></span>

<span data-ttu-id="bbf94-109">如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bbf94-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf94-110">備註</span><span class="sxs-lookup"><span data-stu-id="bbf94-110">Remarks</span></span>

<span data-ttu-id="bbf94-111">Exstrace.dll 是選用的元件，會以 Simple Mail 傳送通訊協定來安裝， (SMTP) 和網路新聞傳輸通訊協定 (NNTP) 。</span><span class="sxs-lookup"><span data-stu-id="bbf94-111">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="bbf94-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="bbf94-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf94-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbf94-113">Requirements</span></span>



| <span data-ttu-id="bbf94-114">需求</span><span class="sxs-lookup"><span data-stu-id="bbf94-114">Requirement</span></span> | <span data-ttu-id="bbf94-115">值</span><span class="sxs-lookup"><span data-stu-id="bbf94-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf94-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bbf94-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bbf94-117"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbf94-117"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
