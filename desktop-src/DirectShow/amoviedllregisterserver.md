---
description: AMovieDllRegisterServer 函式已淘汰。 請改用 AMovieDllRegisterServer2。
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: 'AMovieDllRegisterServer 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099936"
---
# <a name="amoviedllregisterserver-function"></a><span data-ttu-id="e8ddb-104">AMovieDllRegisterServer 函式</span><span class="sxs-lookup"><span data-stu-id="e8ddb-104">AMovieDllRegisterServer function</span></span>

<span data-ttu-id="e8ddb-105">已過時。</span><span class="sxs-lookup"><span data-stu-id="e8ddb-105">Obsolete.</span></span> <span data-ttu-id="e8ddb-106">請改用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 。</span><span class="sxs-lookup"><span data-stu-id="e8ddb-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ddb-107">語法</span><span class="sxs-lookup"><span data-stu-id="e8ddb-107">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="e8ddb-108">參數</span><span class="sxs-lookup"><span data-stu-id="e8ddb-108">Parameters</span></span>

<span data-ttu-id="e8ddb-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="e8ddb-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8ddb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8ddb-110">Return value</span></span>

<span data-ttu-id="e8ddb-111">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e8ddb-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e8ddb-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e8ddb-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8ddb-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8ddb-113">Requirements</span></span>



| <span data-ttu-id="e8ddb-114">需求</span><span class="sxs-lookup"><span data-stu-id="e8ddb-114">Requirement</span></span> | <span data-ttu-id="e8ddb-115">值</span><span class="sxs-lookup"><span data-stu-id="e8ddb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ddb-116">標頭</span><span class="sxs-lookup"><span data-stu-id="e8ddb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e8ddb-117"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e8ddb-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8ddb-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="e8ddb-118">Library</span></span><br/> | <dl> <span data-ttu-id="e8ddb-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e8ddb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8ddb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8ddb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ddb-121">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="e8ddb-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




