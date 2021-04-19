---
description: AMovieDllRegisterServer2 函數會註冊及取消註冊篩選。
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: 'AMovieDllRegisterServer2 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990970"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="7e977-103">AMovieDllRegisterServer2 函式</span><span class="sxs-lookup"><span data-stu-id="7e977-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="7e977-104">**AMovieDllRegisterServer2** 函數會註冊及取消註冊篩選。</span><span class="sxs-lookup"><span data-stu-id="7e977-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e977-105">語法</span><span class="sxs-lookup"><span data-stu-id="7e977-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="7e977-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e977-107">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="7e977-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="7e977-108">**TRUE** 表示註冊篩選準則， **FALSE** 表示將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="7e977-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e977-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e977-109">Return value</span></span>

<span data-ttu-id="7e977-110">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7e977-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7e977-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7e977-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e977-112">備註</span><span class="sxs-lookup"><span data-stu-id="7e977-112">Remarks</span></span>

<span data-ttu-id="7e977-113">您可以使用此函式來設定篩選。</span><span class="sxs-lookup"><span data-stu-id="7e977-113">Use this function to set up your filters.</span></span> <span data-ttu-id="7e977-114">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="7e977-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e977-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e977-115">Requirements</span></span>



| <span data-ttu-id="7e977-116">需求</span><span class="sxs-lookup"><span data-stu-id="7e977-116">Requirement</span></span> | <span data-ttu-id="7e977-117">值</span><span class="sxs-lookup"><span data-stu-id="7e977-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e977-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7e977-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7e977-119"><dt>Dllsetup (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7e977-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e977-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="7e977-120">Library</span></span><br/> | <dl> <span data-ttu-id="7e977-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7e977-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e977-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e977-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e977-123">**DLL 安裝函式**</span><span class="sxs-lookup"><span data-stu-id="7e977-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




