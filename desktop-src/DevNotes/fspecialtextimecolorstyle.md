---
description: 指定指定的色彩是否為特殊的文字色彩。
ms.assetid: 527806f5-5046-48b0-a8db-86a5b8c0db08
title: FSpecialTextIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FSpecialTextIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: cfaf83aeb2fcb03ab61c1280ec821174117026fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978655"
---
# <a name="fspecialtextimecolorstyle-function"></a><span data-ttu-id="805a3-103">FSpecialTextIMEColorStyle 函式</span><span class="sxs-lookup"><span data-stu-id="805a3-103">FSpecialTextIMEColorStyle function</span></span>

<span data-ttu-id="805a3-104">指定指定的色彩是否為特殊的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="805a3-104">Specifies whether the specified color is a special text color.</span></span>

## <a name="syntax"></a><span data-ttu-id="805a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="805a3-105">Syntax</span></span>


```C++
BOOL __cdecl FSpecialTextIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="805a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="805a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805a3-107">*pcolorstyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="805a3-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="805a3-108">從 [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)或 [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)函數傳回的 **IMECOLORSTY** 結構。</span><span class="sxs-lookup"><span data-stu-id="805a3-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805a3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="805a3-109">Return value</span></span>

<span data-ttu-id="805a3-110">當色彩為特殊文字色彩時傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="805a3-110">Returns **TRUE** when the color is a special text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="805a3-111">備註</span><span class="sxs-lookup"><span data-stu-id="805a3-111">Remarks</span></span>

<span data-ttu-id="805a3-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="805a3-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="805a3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="805a3-113">Requirements</span></span>



| <span data-ttu-id="805a3-114">需求</span><span class="sxs-lookup"><span data-stu-id="805a3-114">Requirement</span></span> | <span data-ttu-id="805a3-115">值</span><span class="sxs-lookup"><span data-stu-id="805a3-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="805a3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="805a3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="805a3-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805a3-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805a3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="805a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805a3-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="805a3-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="805a3-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="805a3-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
