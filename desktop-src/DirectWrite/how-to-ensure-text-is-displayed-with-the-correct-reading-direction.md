---
title: 確定文字以正確的閱讀方向顯示
description: 某些語言（例如阿拉伯文和希伯來文）需要由右至左的閱讀方向。
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683075"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="9c727-103">確定文字以正確的閱讀方向顯示</span><span class="sxs-lookup"><span data-stu-id="9c727-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="9c727-104">某些語言（例如阿拉伯文和希伯來文）需要由右至左的閱讀方向。</span><span class="sxs-lookup"><span data-stu-id="9c727-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="9c727-105">若為 [DirectWrite](direct-write-portal.md) 的文字格式物件，預設的閱讀方向為從左至右。</span><span class="sxs-lookup"><span data-stu-id="9c727-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="9c727-106">DirectWrite 不會自動從地區設定推斷讀取方向，因此您必須自行進行。</span><span class="sxs-lookup"><span data-stu-id="9c727-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="9c727-107">首先，使用 windowsx 中定義的 GetWindowStyleEx 宏，取得要轉譯文字之視窗的擴充樣式旗標。</span><span class="sxs-lookup"><span data-stu-id="9c727-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="9c727-108">宏會傳回由數個旗標所組成的 DWORD 值，並結合了位 OR 運算。</span><span class="sxs-lookup"><span data-stu-id="9c727-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="9c727-109">您必須判斷是否有影響讀取方向的特定旗標。</span><span class="sxs-lookup"><span data-stu-id="9c727-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="9c727-110">有兩個不同的旗標與閱讀方向相關： WS \_ ex \_ LAYOUTRTL 和 ws \_ ex \_ RTLREADING。</span><span class="sxs-lookup"><span data-stu-id="9c727-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="9c727-111">使用位 AND 運算子 (&) 搭配 dwStyle 變數和 WS \_ EX \_ LAYOUTRTL 宏來儲存布林值，指出配置是否經過鏡像處理。</span><span class="sxs-lookup"><span data-stu-id="9c727-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="9c727-112">針對 WS \_ EX RTLREADING 旗標進行相同的動作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9c727-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="9c727-113">使用 [**IDWriteTextFormat：： SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) 方法設定讀取方向。</span><span class="sxs-lookup"><span data-stu-id="9c727-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="9c727-114">預設值為從左至右，因此您只需要設定從右至左的讀取方向。</span><span class="sxs-lookup"><span data-stu-id="9c727-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="9c727-115">WS \_ EX \_ LAYOUTRTL 會鏡像整個版面配置，並隱含由右至左的閱讀方向，因此只有在其中一個旗標存在時，才會設定閱讀方向。</span><span class="sxs-lookup"><span data-stu-id="9c727-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="9c727-116">如果兩者都存在，則會彼此取消，而文字格式的讀取方向應該是由左至右。</span><span class="sxs-lookup"><span data-stu-id="9c727-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
