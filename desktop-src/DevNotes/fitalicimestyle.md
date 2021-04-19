---
description: 指定非色彩樣式是否具有斜體樣式。
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: FItalicIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996198"
---
# <a name="fitalicimestyle-function"></a><span data-ttu-id="46158-103">FItalicIMEStyle 函式</span><span class="sxs-lookup"><span data-stu-id="46158-103">FItalicIMEStyle function</span></span>

<span data-ttu-id="46158-104">指定非色彩樣式是否具有斜體樣式。</span><span class="sxs-lookup"><span data-stu-id="46158-104">Specifies whether a non-color style has the italic style.</span></span>

## <a name="syntax"></a><span data-ttu-id="46158-105">語法</span><span class="sxs-lookup"><span data-stu-id="46158-105">Syntax</span></span>


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="46158-106">參數</span><span class="sxs-lookup"><span data-stu-id="46158-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46158-107">*pimestyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46158-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46158-108">從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="46158-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46158-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="46158-109">Return value</span></span>

<span data-ttu-id="46158-110">如果樣式具有斜體樣式，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="46158-110">**TRUE** if the style has the italic style.</span></span>

## <a name="remarks"></a><span data-ttu-id="46158-111">備註</span><span class="sxs-lookup"><span data-stu-id="46158-111">Remarks</span></span>

<span data-ttu-id="46158-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="46158-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="46158-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="46158-113">Requirements</span></span>



| <span data-ttu-id="46158-114">需求</span><span class="sxs-lookup"><span data-stu-id="46158-114">Requirement</span></span> | <span data-ttu-id="46158-115">值</span><span class="sxs-lookup"><span data-stu-id="46158-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46158-116">DLL</span><span class="sxs-lookup"><span data-stu-id="46158-116">DLL</span></span><br/> | <dl> <span data-ttu-id="46158-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46158-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46158-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46158-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46158-119">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="46158-119">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
