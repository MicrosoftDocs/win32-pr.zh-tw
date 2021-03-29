---
Description: COLORRE光圈值是用來指定 RGB 色彩。
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: 'COLORREF (Windef) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992451"
---
# <a name="colorref"></a><span data-ttu-id="8f92f-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="8f92f-103">COLORREF</span></span>

<span data-ttu-id="8f92f-104">COLORRE光圈值是用來指定 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 色彩。</span><span class="sxs-lookup"><span data-stu-id="8f92f-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="8f92f-105">備註</span><span class="sxs-lookup"><span data-stu-id="8f92f-105">Remarks</span></span>

<span data-ttu-id="8f92f-106">指定明確的 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 色彩時， **COLORREF** 值的十六進位形式如下：</span><span class="sxs-lookup"><span data-stu-id="8f92f-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="8f92f-107">低序位位元組包含相對強度的紅色值;第二個位元組包含綠色的值;第三個位元組包含藍色的值。</span><span class="sxs-lookup"><span data-stu-id="8f92f-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="8f92f-108">高序位位元組必須為零。</span><span class="sxs-lookup"><span data-stu-id="8f92f-108">The high-order byte must be zero.</span></span> <span data-ttu-id="8f92f-109">單一位元組的最大值是0xFF。</span><span class="sxs-lookup"><span data-stu-id="8f92f-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="8f92f-110">若要建立 **COLORREF** 色彩值，請使用 [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) 宏。</span><span class="sxs-lookup"><span data-stu-id="8f92f-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="8f92f-111">若要將色彩值的紅色、綠色和藍色元件的個別值解壓縮，請分別使用 [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)、 [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)和 [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) 宏。</span><span class="sxs-lookup"><span data-stu-id="8f92f-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="8f92f-112">範例</span><span class="sxs-lookup"><span data-stu-id="8f92f-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="8f92f-113">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="8f92f-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f92f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f92f-114">Requirements</span></span>



| <span data-ttu-id="8f92f-115">需求</span><span class="sxs-lookup"><span data-stu-id="8f92f-115">Requirement</span></span> | <span data-ttu-id="8f92f-116">值</span><span class="sxs-lookup"><span data-stu-id="8f92f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f92f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f92f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f92f-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f92f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8f92f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f92f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f92f-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f92f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f92f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8f92f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f92f-122"><dt>Windef (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="8f92f-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f92f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f92f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f92f-124">色彩總覽</span><span class="sxs-lookup"><span data-stu-id="8f92f-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="8f92f-125">色彩結構</span><span class="sxs-lookup"><span data-stu-id="8f92f-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="8f92f-126">GetBValue</span><span class="sxs-lookup"><span data-stu-id="8f92f-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="8f92f-127">GetGValue</span><span class="sxs-lookup"><span data-stu-id="8f92f-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="8f92f-128">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="8f92f-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="8f92f-129">RGB</span><span class="sxs-lookup"><span data-stu-id="8f92f-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




