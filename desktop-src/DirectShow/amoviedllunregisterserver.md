---
description: AMovieDllUnregisterServer 函式已淘汰。 請改用 AMovieDllRegisterServer2。
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
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099926"
---
# <a name="amoviedllunregisterserver-function"></a><span data-ttu-id="9b16f-104">AMovieDllUnregisterServer 函式</span><span class="sxs-lookup"><span data-stu-id="9b16f-104">AMovieDllUnregisterServer function</span></span>

<span data-ttu-id="9b16f-105">已過時。</span><span class="sxs-lookup"><span data-stu-id="9b16f-105">Obsolete.</span></span> <span data-ttu-id="9b16f-106">請改用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 。</span><span class="sxs-lookup"><span data-stu-id="9b16f-106">Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b16f-107">語法</span><span class="sxs-lookup"><span data-stu-id="9b16f-107">Syntax</span></span>


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a><span data-ttu-id="9b16f-108">參數</span><span class="sxs-lookup"><span data-stu-id="9b16f-108">Parameters</span></span>

<span data-ttu-id="9b16f-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="9b16f-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b16f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b16f-110">Return value</span></span>

<span data-ttu-id="9b16f-111">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9b16f-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b16f-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9b16f-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b16f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b16f-113">Requirements</span></span>



| <span data-ttu-id="9b16f-114">需求</span><span class="sxs-lookup"><span data-stu-id="9b16f-114">Requirement</span></span> | <span data-ttu-id="9b16f-115">值</span><span class="sxs-lookup"><span data-stu-id="9b16f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b16f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="9b16f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9b16f-117"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9b16f-117"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9b16f-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="9b16f-118">Library</span></span><br/> | <dl> <span data-ttu-id="9b16f-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9b16f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b16f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b16f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b16f-121">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="9b16f-121">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




