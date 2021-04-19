---
description: 指定指定的色彩是否為 Windows 色彩。
ms.assetid: 0d2b2039-938c-4f9d-8ddc-9eb711f55009
title: FWinIMEColorStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FWinIMEColorStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 28731672f5f1aff385f9051ba8b641b7cdcdf83c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989538"
---
# <a name="fwinimecolorstyle-function"></a><span data-ttu-id="6ed3d-103">FWinIMEColorStyle 函式</span><span class="sxs-lookup"><span data-stu-id="6ed3d-103">FWinIMEColorStyle function</span></span>

<span data-ttu-id="6ed3d-104">指定指定的色彩是否為 Windows 色彩。</span><span class="sxs-lookup"><span data-stu-id="6ed3d-104">Specifies whether the specified color is a Windows color.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed3d-105">語法</span><span class="sxs-lookup"><span data-stu-id="6ed3d-105">Syntax</span></span>


```C++
BOOL __cdecl FWinIMEColorStyle(
  _In_ const IMECOLORSTY *pcolorstyle
);
```



## <a name="parameters"></a><span data-ttu-id="6ed3d-106">參數</span><span class="sxs-lookup"><span data-stu-id="6ed3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ed3d-107">*pcolorstyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ed3d-107">*pcolorstyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ed3d-108">從 [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md)或 [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md)函數傳回的 **IMECOLORSTY** 結構。</span><span class="sxs-lookup"><span data-stu-id="6ed3d-108">An **IMECOLORSTY** structure returned from a [**PColorStyleBackFromIMEStyle**](pcolorstylebackfromimestyle.md) or [**PColorStyleTextFromIMEStyle**](pcolorstyletextfromimestyle.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ed3d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ed3d-109">Return value</span></span>

<span data-ttu-id="6ed3d-110">當色彩為 Windows 色彩時傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6ed3d-110">Returns **TRUE** when the color is a Windows color.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ed3d-111">備註</span><span class="sxs-lookup"><span data-stu-id="6ed3d-111">Remarks</span></span>

<span data-ttu-id="6ed3d-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="6ed3d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ed3d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ed3d-113">Requirements</span></span>



| <span data-ttu-id="6ed3d-114">需求</span><span class="sxs-lookup"><span data-stu-id="6ed3d-114">Requirement</span></span> | <span data-ttu-id="6ed3d-115">值</span><span class="sxs-lookup"><span data-stu-id="6ed3d-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ed3d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6ed3d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6ed3d-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ed3d-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ed3d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ed3d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed3d-119">**PColorStyleBackFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="6ed3d-119">**PColorStyleBackFromIMEStyle**</span></span>](pcolorstylebackfromimestyle.md)
</dt> <dt>

[<span data-ttu-id="6ed3d-120">**PColorStyleTextFromIMEStyle**</span><span class="sxs-lookup"><span data-stu-id="6ed3d-120">**PColorStyleTextFromIMEStyle**</span></span>](pcolorstyletextfromimestyle.md)
</dt> </dl>

 

 
