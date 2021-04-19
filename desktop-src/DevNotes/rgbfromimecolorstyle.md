---
description: 將 IMECOLORSTY 結構轉換成 COLORREF 結構。
ms.assetid: f7a3eab0-16ca-4c4e-9eda-bead8d1a91b8
title: RGBFromIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RGBFromIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 7993253e5e11c45cae3e062467db080201bc1228
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997670"
---
# <a name="rgbfromimecolorstyle-function"></a><span data-ttu-id="cc200-103">RGBFromIMEColorStyle 函式</span><span class="sxs-lookup"><span data-stu-id="cc200-103">RGBFromIMEColorStyle function</span></span>

<span data-ttu-id="cc200-104">將 **IMECOLORSTY** 結構轉換成 [**COLORREF**](../gdi/colorref.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="cc200-104">Converts an **IMECOLORSTY** structure to a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc200-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc200-105">Syntax</span></span>


```C++
COLORREF RGBFromIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="cc200-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc200-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc200-107">*pcolorstyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc200-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc200-108">從 [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)或 [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)函數傳回的 **IMECOLORSTY** 結構。</span><span class="sxs-lookup"><span data-stu-id="cc200-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc200-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc200-109">Return value</span></span>

<span data-ttu-id="cc200-110">傳回 [**COLORREF**](../gdi/colorref.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="cc200-110">Returns a [**COLORREF**](../gdi/colorref.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc200-111">備註</span><span class="sxs-lookup"><span data-stu-id="cc200-111">Remarks</span></span>

<span data-ttu-id="cc200-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="cc200-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc200-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc200-113">Requirements</span></span>



| <span data-ttu-id="cc200-114">需求</span><span class="sxs-lookup"><span data-stu-id="cc200-114">Requirement</span></span> | <span data-ttu-id="cc200-115">值</span><span class="sxs-lookup"><span data-stu-id="cc200-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc200-116">DLL</span><span class="sxs-lookup"><span data-stu-id="cc200-116">DLL</span></span><br/> | <dl> <span data-ttu-id="cc200-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc200-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc200-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc200-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc200-119">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="cc200-119">**COLORREF**</span></span>](../gdi/colorref.md)
</dt> <dt>

[<span data-ttu-id="cc200-120">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="cc200-120">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="cc200-121">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="cc200-121">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
