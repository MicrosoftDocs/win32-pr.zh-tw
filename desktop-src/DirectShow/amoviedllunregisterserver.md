---
description: 已過時。 請改用 AMovieDllRegisterServer2。
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: 'AMovieDllUnregisterServer 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4cab526a69f14cdd4c4f48767ca34722f61002eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000934"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="113e2-104">AMovieDllUnregisterServer 函式</span><span class="sxs-lookup"><span data-stu-id="113e2-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="113e2-105">已過時。</span><span class="sxs-lookup"><span data-stu-id="113e2-105">Obsolete.</span></span> <span data-ttu-id="113e2-106">請改用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 。</span><span class="sxs-lookup"><span data-stu-id="113e2-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="113e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="113e2-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="113e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="113e2-108">Parameters</span></span>

<span data-ttu-id="113e2-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="113e2-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="113e2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="113e2-110">Return value</span></span>

<span data-ttu-id="113e2-111">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="113e2-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="113e2-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="113e2-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="113e2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="113e2-113">Requirements</span></span>



| <span data-ttu-id="113e2-114">需求</span><span class="sxs-lookup"><span data-stu-id="113e2-114">Requirement</span></span> | <span data-ttu-id="113e2-115">值</span><span class="sxs-lookup"><span data-stu-id="113e2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="113e2-116">標頭</span><span class="sxs-lookup"><span data-stu-id="113e2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="113e2-117"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="113e2-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="113e2-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="113e2-118">Library</span></span><br/> | <dl> <span data-ttu-id="113e2-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="113e2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="113e2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="113e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113e2-121">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="113e2-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




