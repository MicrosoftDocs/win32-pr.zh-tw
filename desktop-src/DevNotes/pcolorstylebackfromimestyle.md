---
description: 抓取指定樣式的背景色彩樣式。
ms.assetid: 1b0acac1-c36d-49b6-8154-f69bda008e9a
title: PColorStyleBackFromIMEStyle 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PColorStyleBackFromIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 33ff9072fc5e850654f932817cd4ecf0e9372aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989843"
---
# <a name="pcolorstylebackfromimestyle-function"></a><span data-ttu-id="9f8f2-103">PColorStyleBackFromIMEStyle 函式</span><span class="sxs-lookup"><span data-stu-id="9f8f2-103">PColorStyleBackFromIMEStyle function</span></span>

<span data-ttu-id="9f8f2-104">抓取指定樣式的背景色彩樣式。</span><span class="sxs-lookup"><span data-stu-id="9f8f2-104">Retrieves the background color style of the specified style.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f8f2-105">Syntax</span></span>


```C++
const IMECOLORSTY* __cdecl PColorStyleBackFromIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a><span data-ttu-id="9f8f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f8f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f8f2-107">*pimestyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f8f2-107">*pimestyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8f2-108">從 [**PIMEStyleFromAttr**](pimestylefromattr.md)函數傳回的 **IMESTYLE** 結構。</span><span class="sxs-lookup"><span data-stu-id="9f8f2-108">An **IMESTYLE** structure returned from [**PIMEStyleFromAttr**](pimestylefromattr.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f8f2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f8f2-109">Return value</span></span>

<span data-ttu-id="9f8f2-110">**IMECOLORSTY** 結構的指標，表示背景色彩樣式。</span><span class="sxs-lookup"><span data-stu-id="9f8f2-110">Pointer to an **IMECOLORSTY** structure representing the background color style.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f8f2-111">備註</span><span class="sxs-lookup"><span data-stu-id="9f8f2-111">Remarks</span></span>

<span data-ttu-id="9f8f2-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9f8f2-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="9f8f2-113">**IMECOLORSTY** 結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="9f8f2-113">The **IMECOLORSTY** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    UINT colorId;
    union {
        COLORREF    rgb;
        UINT        colorWin;
        UINT        colorSpec;
        UINT        colorFund;
    };
} IMECOLORSTY;
```

## <a name="requirements"></a><span data-ttu-id="9f8f2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f8f2-114">Requirements</span></span>



| <span data-ttu-id="9f8f2-115">需求</span><span class="sxs-lookup"><span data-stu-id="9f8f2-115">Requirement</span></span> | <span data-ttu-id="9f8f2-116">值</span><span class="sxs-lookup"><span data-stu-id="9f8f2-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8f2-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8f2-117">DLL</span></span><br/> | <dl> <span data-ttu-id="9f8f2-118"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8f2-118"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f8f2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f8f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f8f2-120">**PIMEStyleFromAttr**</span><span class="sxs-lookup"><span data-stu-id="9f8f2-120">**PIMEStyleFromAttr**</span></span>](pimestylefromattr.md)
</dt> </dl>

 

 
