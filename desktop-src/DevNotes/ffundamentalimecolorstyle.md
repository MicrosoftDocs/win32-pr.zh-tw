---
description: 指定指定的色彩是否為基本色彩。
ms.assetid: 9a06fadc-9b97-4f7d-9488-688b72d14bc5
title: FFundamentalIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FFundamentalIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: c7de1bf4ef84d159d673e1039ad6ea328153b216
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000825"
---
# <a name="ffundamentalimecolorstyle-function"></a><span data-ttu-id="8007b-103">FFundamentalIMEColorStyle 函式</span><span class="sxs-lookup"><span data-stu-id="8007b-103">FFundamentalIMEColorStyle function</span></span>

<span data-ttu-id="8007b-104">指定指定的色彩是否為基本色彩。</span><span class="sxs-lookup"><span data-stu-id="8007b-104">Specifies whether the specified color is a fundamental color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8007b-105">語法</span><span class="sxs-lookup"><span data-stu-id="8007b-105">Syntax</span></span>


```C++
BOOL __cdecl FFundamentalIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="8007b-106">參數</span><span class="sxs-lookup"><span data-stu-id="8007b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8007b-107">*pcolorstyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8007b-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8007b-108">從 [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)或 [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)函數傳回的 **IMECOLORSTY** 結構。</span><span class="sxs-lookup"><span data-stu-id="8007b-108">An **IMECOLORSTY** structure returned from the [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8007b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8007b-109">Return value</span></span>

<span data-ttu-id="8007b-110">當色彩為基本色彩時傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="8007b-110">Returns **TRUE** when the color is a fundamental color.</span></span>

## <a name="remarks"></a><span data-ttu-id="8007b-111">備註</span><span class="sxs-lookup"><span data-stu-id="8007b-111">Remarks</span></span>

<span data-ttu-id="8007b-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="8007b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8007b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8007b-113">Requirements</span></span>



| <span data-ttu-id="8007b-114">需求</span><span class="sxs-lookup"><span data-stu-id="8007b-114">Requirement</span></span> | <span data-ttu-id="8007b-115">值</span><span class="sxs-lookup"><span data-stu-id="8007b-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8007b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8007b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8007b-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8007b-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8007b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8007b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8007b-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="8007b-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="8007b-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="8007b-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
