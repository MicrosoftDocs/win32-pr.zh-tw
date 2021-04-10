---
title: 如何支援回呼專案
description: 本主題將示範如何提供回呼專案的支援。
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933726"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="d590b-103">如何支援回呼專案</span><span class="sxs-lookup"><span data-stu-id="d590b-103">How to Support Callback Items</span></span>

<span data-ttu-id="d590b-104">本主題將示範如何提供回呼專案的支援。</span><span class="sxs-lookup"><span data-stu-id="d590b-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="d590b-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="d590b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d590b-106">技術</span><span class="sxs-lookup"><span data-stu-id="d590b-106">Technologies</span></span>

-   [<span data-ttu-id="d590b-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="d590b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="d590b-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="d590b-108">Prerequisites</span></span>

-   <span data-ttu-id="d590b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="d590b-109">C/C++</span></span>
-   <span data-ttu-id="d590b-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="d590b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="d590b-111">指示</span><span class="sxs-lookup"><span data-stu-id="d590b-111">Instructions</span></span>


<span data-ttu-id="d590b-112">如果您的應用程式將會使用 ComboBoxEx 控制項中的回呼專案，必須準備好處理 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="d590b-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="d590b-113">ComboBoxEx 控制項會在需要擁有者來提供特定專案資訊時傳送此通知。</span><span class="sxs-lookup"><span data-stu-id="d590b-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="d590b-114">如需回呼專案的詳細資訊，請參閱 [回呼專案](comboboxex-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="d590b-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="d590b-115">下列應用程式定義函式會藉由提供指定專案的屬性來處理 [CBEN \_ GETDISPINFO](cben-getdispinfo.md) 。</span><span class="sxs-lookup"><span data-stu-id="d590b-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="d590b-116">請注意，它會將傳入 [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的 **遮罩** 成員設定為 CBEIF \_ DI \_ SETITEM。</span><span class="sxs-lookup"><span data-stu-id="d590b-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="d590b-117">將 **mask** 設定為這個值會讓控制項保留專案資訊，讓它不需要再次要求資訊。</span><span class="sxs-lookup"><span data-stu-id="d590b-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="d590b-118">完整範例</span><span class="sxs-lookup"><span data-stu-id="d590b-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="d590b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="d590b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d590b-120">關於 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="d590b-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="d590b-121">ComboBoxEx 控制項參考</span><span class="sxs-lookup"><span data-stu-id="d590b-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d590b-122">使用 ComboBoxEx 控制項</span><span class="sxs-lookup"><span data-stu-id="d590b-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="d590b-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="d590b-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 