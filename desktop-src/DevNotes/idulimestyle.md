---
description: 識別指定的非色彩樣式是否有底線。
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: IdUlIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001921"
---
# <a name="idulimestyle-function"></a><span data-ttu-id="3232b-103">IdUlIMEStyle 函式</span><span class="sxs-lookup"><span data-stu-id="3232b-103">IdUlIMEStyle function</span></span>

<span data-ttu-id="3232b-104">識別指定的非色彩樣式是否有底線。</span><span class="sxs-lookup"><span data-stu-id="3232b-104">Identifies whether the specified non-color style has underline.</span></span>

## <a name="syntax"></a><span data-ttu-id="3232b-105">語法</span><span class="sxs-lookup"><span data-stu-id="3232b-105">Syntax</span></span>


```C++
UINT __cdecl IdUlIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="3232b-106">參數</span><span class="sxs-lookup"><span data-stu-id="3232b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3232b-107">*pimestyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3232b-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3232b-108">從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="3232b-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3232b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3232b-109">Return value</span></span>

<span data-ttu-id="3232b-110">此函數可以傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3232b-110">This function can returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3232b-111">**IMESTY \_UL \_ MIN** (2002) </span><span class="sxs-lookup"><span data-stu-id="3232b-111">**IMESTY\_UL\_MIN** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-112">**IMESTY \_UL \_ 無** (2002) </span><span class="sxs-lookup"><span data-stu-id="3232b-112">**IMESTY\_UL\_NONE** (2002)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-113">**IMESTY \_UL \_ SINGLE** (2003) </span><span class="sxs-lookup"><span data-stu-id="3232b-113">**IMESTY\_UL\_SINGLE** (2003)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-114">**IMESTY \_UL \_ 虛線** (2005) </span><span class="sxs-lookup"><span data-stu-id="3232b-114">**IMESTY\_UL\_DOTTED** (2005)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-115">**IMESTY \_UL \_ 厚** (2006) </span><span class="sxs-lookup"><span data-stu-id="3232b-115">**IMESTY\_UL\_THICK** (2006)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-116">**IMESTY \_UL \_ 低** (2011) </span><span class="sxs-lookup"><span data-stu-id="3232b-116">**IMESTY\_UL\_LOWER** (2011)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-117">**IMESTY \_UL \_ THICKLOWER** (2012) </span><span class="sxs-lookup"><span data-stu-id="3232b-117">**IMESTY\_UL\_THICKLOWER** (2012)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-118">**IMESTY \_UL \_ THICKDITHLOWER** (2013) </span><span class="sxs-lookup"><span data-stu-id="3232b-118">**IMESTY\_UL\_THICKDITHLOWER** (2013)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-119">**IMESTY \_UL \_ DITHLOWER** (2014) </span><span class="sxs-lookup"><span data-stu-id="3232b-119">**IMESTY\_UL\_DITHLOWER** (2014)</span></span>
</dt> <dt>

<span data-ttu-id="3232b-120">**IMESTY \_UL \_ MAX** (2014) </span><span class="sxs-lookup"><span data-stu-id="3232b-120">**IMESTY\_UL\_MAX** (2014)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="3232b-121">備註</span><span class="sxs-lookup"><span data-stu-id="3232b-121">Remarks</span></span>

<span data-ttu-id="3232b-122">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="3232b-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3232b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3232b-123">Requirements</span></span>



| <span data-ttu-id="3232b-124">需求</span><span class="sxs-lookup"><span data-stu-id="3232b-124">Requirement</span></span> | <span data-ttu-id="3232b-125">值</span><span class="sxs-lookup"><span data-stu-id="3232b-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3232b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3232b-126">DLL</span></span><br/> | <dl> <span data-ttu-id="3232b-127"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3232b-127"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3232b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3232b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3232b-129">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="3232b-129">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
