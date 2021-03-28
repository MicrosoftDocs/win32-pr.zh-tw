---
description: 系統提供六種股票字型。
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: 使用股票字型來繪製文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945013"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="e85aa-103">使用股票字型來繪製文字</span><span class="sxs-lookup"><span data-stu-id="e85aa-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="e85aa-104">系統提供六種股票字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-104">The system provides six stock fonts.</span></span> <span data-ttu-id="e85aa-105">股票字型是一種邏輯字型，可讓應用程式藉由呼叫 [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 函式並指定要求的字型來取得。</span><span class="sxs-lookup"><span data-stu-id="e85aa-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="e85aa-106">下列清單包含您可以指定的值，以取得股票字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="e85aa-107">值</span><span class="sxs-lookup"><span data-stu-id="e85aa-107">Value</span></span>                 | <span data-ttu-id="e85aa-108">意義</span><span class="sxs-lookup"><span data-stu-id="e85aa-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85aa-109">ANSI \_ 固定 \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="e85aa-110">根據 Windows 字元集指定等寬字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="e85aa-111">通常會使用一個宋體。</span><span class="sxs-lookup"><span data-stu-id="e85aa-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="e85aa-112">ANSI \_ VAR \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="e85aa-113">根據 Windows 字元集指定比例字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="e85aa-114">通常會使用 MS Sans Serif。</span><span class="sxs-lookup"><span data-stu-id="e85aa-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="e85aa-115">裝置 \_ 預設 \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="e85aa-116">指定指定裝置的慣用字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="e85aa-117">這通常是顯示裝置的系統字型;不過，對於某些點矩陣印表機，這是在裝置上的字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="e85aa-118">使用這個字型 (列印的速度通常比使用下載的點陣圖字型) 的列印速度還要快。</span><span class="sxs-lookup"><span data-stu-id="e85aa-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="e85aa-119">OEM \_ 固定 \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="e85aa-120">根據 OEM 字元集指定等寬字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="e85aa-121">針對 IBM 電腦和 compatibles，OEM 字型是以 IBM PC 字元集為基礎。</span><span class="sxs-lookup"><span data-stu-id="e85aa-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="e85aa-122">系統 \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="e85aa-123">指定系統字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-123">Specifies the System font.</span></span> <span data-ttu-id="e85aa-124">這是根據 Windows 字元集的比例字型，由作業系統用來顯示視窗標題、功能表名稱，以及對話方塊中的文字。</span><span class="sxs-lookup"><span data-stu-id="e85aa-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="e85aa-125">系統字型一律可供使用。</span><span class="sxs-lookup"><span data-stu-id="e85aa-125">The System font is always available.</span></span> <span data-ttu-id="e85aa-126">其他字型則只有在已安裝時才可使用。</span><span class="sxs-lookup"><span data-stu-id="e85aa-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="e85aa-127">系統 \_ 固定 \_ 字型</span><span class="sxs-lookup"><span data-stu-id="e85aa-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="e85aa-128">指定與舊版 Windows 中的系統字型相容的等寬字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="e85aa-129">如需字型的詳細資訊，請參閱 [關於](about-fonts.md)字型。</span><span class="sxs-lookup"><span data-stu-id="e85aa-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="e85aa-130">下列範例會取出變數股票字型的控制碼、將其選取為裝置內容，然後使用該字型來寫入字串：</span><span class="sxs-lookup"><span data-stu-id="e85aa-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="e85aa-131">如果無法使用其他股票字型， [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) 會傳回系統字型的控制碼 (系統 \_ 字型) 。</span><span class="sxs-lookup"><span data-stu-id="e85aa-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="e85aa-132">只有當應用程式的裝置內容的對應模式是 MM TEXT 時，才應該使用股票字型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e85aa-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



