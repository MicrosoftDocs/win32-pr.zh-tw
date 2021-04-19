---
description: 取得指定屬性的樣式。
ms.assetid: 206c69b9-981b-49ef-9f71-1c65e08637bb
title: PIMEStyleFromAttr 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PIMEStyleFromAttr
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 27673ebb74c1dca3e686542a541735cfc515bee9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990102"
---
# <a name="pimestylefromattr-function"></a><span data-ttu-id="8e65f-103">PIMEStyleFromAttr 函式</span><span class="sxs-lookup"><span data-stu-id="8e65f-103">PIMEStyleFromAttr function</span></span>

<span data-ttu-id="8e65f-104">取得指定屬性的樣式。</span><span class="sxs-lookup"><span data-stu-id="8e65f-104">Retrieves styles for a given attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e65f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e65f-105">Syntax</span></span>


```C++
const IMESTYLE* __cdecl PIMEStyleFromAttr(
  _In_ const  UINT attr
);
```



## <a name="parameters"></a><span data-ttu-id="8e65f-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e65f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e65f-107">*attr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8e65f-107">*attr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e65f-108">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8e65f-108">This parameter can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8e65f-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR \_FIXEDCONVERTED** (5) </span><span class="sxs-lookup"><span data-stu-id="8e65f-109"><span id="IMESATTR_FIXEDCONVERTED"></span><span id="imesattr_fixedconverted"></span>**IMESATTR\_FIXEDCONVERTED** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR \_輸入** (0) </span><span class="sxs-lookup"><span data-stu-id="8e65f-110"><span id="IMESATTR_INPUT"></span><span id="imesattr_input"></span>**IMESATTR\_INPUT** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR \_輸入 \_ 錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="8e65f-111"><span id="IMESATTR_INPUT_ERROR"></span><span id="imesattr_input_error"></span>**IMESATTR\_INPUT\_ERROR** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR \_最大** (5) </span><span class="sxs-lookup"><span data-stu-id="8e65f-112"><span id="IMESATTR_MAX"></span><span id="imesattr_max"></span>**IMESATTR\_MAX** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR \_最小** (0) </span><span class="sxs-lookup"><span data-stu-id="8e65f-113"><span id="IMESATTR_MIN"></span><span id="imesattr_min"></span>**IMESATTR\_MIN** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR \_目標 \_ 轉換** (1) </span><span class="sxs-lookup"><span data-stu-id="8e65f-114"><span id="IMESATTR_TARGET_CONVERTED"></span><span id="imesattr_target_converted"></span>**IMESATTR\_TARGET\_CONVERTED** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8e65f-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR \_目標 \_ NOTCONVERTED** (4) </span><span class="sxs-lookup"><span data-stu-id="8e65f-115"><span id="IMESATTR_TARGET_NOTCONVERTED"></span><span id="imesattr_target_notconverted"></span>**IMESATTR\_TARGET\_NOTCONVERTED** (4)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e65f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e65f-116">Return value</span></span>

<span data-ttu-id="8e65f-117">傳回代表色彩和非色彩設定之 **IMESTYLE** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8e65f-117">Returns a pointer to an **IMESTYLE** structure representing the color and non-color settings.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e65f-118">備註</span><span class="sxs-lookup"><span data-stu-id="8e65f-118">Remarks</span></span>

<span data-ttu-id="8e65f-119">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="8e65f-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="8e65f-120">**IMESTYLE** 結構的定義如下：</span><span class="sxs-lookup"><span data-stu-id="8e65f-120">The **IMESTYLE** structure is defined as follows:</span></span>

``` syntax
typedef struct {
    union {
        GRFSTY  grfsty;
        struct {
            UINT    fBold:1;
            UINT    fItalic:1;
            UINT    fUl:1;
            UINT    idUl:(sizeof(UINT) * 8 - 3);
        };
    };

    union {
        IMECOLORSTY colorstyText;
        struct {
            UINT    colorIdText;
            union {
                COLORREF    rgbText;
                UINT        colorWinText;
                UINT        colorSpecText;
                UINT        colorFundText;
            };
        };
    };

    union {
        IMECOLORSTY colorstyBack;
        struct {
            UINT    colorIdBack;
            union {
                COLORREF    rgbBack;
                UINT        colorWinBack;
                UINT        colorSpecBack;
                UINT        colorFundBack;
            };
        };
    };

    union {
        IMECOLORSTY colorstyUl;
        struct {
            UINT    colorIdUl;
            union {
                COLORREF    rgbUl;
                UINT        colorWinUl;
                UINT        colorSpecUl;
                UINT        colorFundUl;
            };
        };
    };
} IMESTYLE;
```

## <a name="requirements"></a><span data-ttu-id="8e65f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e65f-121">Requirements</span></span>



| <span data-ttu-id="8e65f-122">需求</span><span class="sxs-lookup"><span data-stu-id="8e65f-122">Requirement</span></span> | <span data-ttu-id="8e65f-123">值</span><span class="sxs-lookup"><span data-stu-id="8e65f-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e65f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8e65f-124">DLL</span></span><br/> | <dl> <span data-ttu-id="8e65f-125"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e65f-125"><dt>Imeshare.dll</dt></span></span> </dl> |



 

 
