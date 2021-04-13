---
description: 步驟 4：
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: 步驟 4： 建立屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195607"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="fe234-104">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="fe234-104">Step 4.</span></span> <span data-ttu-id="fe234-105">建立屬性頁</span><span class="sxs-lookup"><span data-stu-id="fe234-105">Create the Property Page</span></span>

<span data-ttu-id="fe234-106">此時，篩選器會支援屬性頁面所需的所有專案。</span><span class="sxs-lookup"><span data-stu-id="fe234-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="fe234-107">下一步是執行屬性頁本身。</span><span class="sxs-lookup"><span data-stu-id="fe234-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="fe234-108">首先從 **CBasePropertyPage** 衍生新的類別。</span><span class="sxs-lookup"><span data-stu-id="fe234-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="fe234-109">下列範例會顯示部分宣告，包括稍後將在範例中使用的一些私用成員變數：</span><span class="sxs-lookup"><span data-stu-id="fe234-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="fe234-110">接下來，在資源編輯器中建立對話方塊資源，以及對話方塊標題的字串資源。</span><span class="sxs-lookup"><span data-stu-id="fe234-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="fe234-111">字串會出現在屬性頁的索引標籤中。</span><span class="sxs-lookup"><span data-stu-id="fe234-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="fe234-112">這兩個資源識別碼是 **CBasePropertyPage** 函式的引數：</span><span class="sxs-lookup"><span data-stu-id="fe234-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="fe234-113">下圖顯示 [範例] 屬性頁的對話方塊資源。</span><span class="sxs-lookup"><span data-stu-id="fe234-113">The following illustration shows the dialog resource for the example property page.</span></span>

![屬性頁對話方塊](images/proppage.png)

<span data-ttu-id="fe234-115">現在您已準備好執行屬性頁。</span><span class="sxs-lookup"><span data-stu-id="fe234-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="fe234-116">以下是 **CBasePropertyPage** 中要覆寫的方法：</span><span class="sxs-lookup"><span data-stu-id="fe234-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="fe234-117">當用戶端建立屬性頁時，會呼叫 **OnConnect** 。</span><span class="sxs-lookup"><span data-stu-id="fe234-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="fe234-118">它會將 **IUnknown** 指標設定為篩選器。</span><span class="sxs-lookup"><span data-stu-id="fe234-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="fe234-119">建立對話方塊時，會呼叫 **OnActivate** 。</span><span class="sxs-lookup"><span data-stu-id="fe234-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="fe234-120">當對話方塊收到視窗訊息時，就會呼叫 **OnReceiveMessage** 。</span><span class="sxs-lookup"><span data-stu-id="fe234-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="fe234-121">當使用者按一下 [**確定]** **或 [** 套用] 按鈕來認可屬性變更時，就會呼叫 **OnApplyChanges** 。</span><span class="sxs-lookup"><span data-stu-id="fe234-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="fe234-122">當使用者關閉屬性工作表時，就會呼叫 **OnDisconnect** 。</span><span class="sxs-lookup"><span data-stu-id="fe234-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="fe234-123">本教學課程的其餘部分將說明這些方法。</span><span class="sxs-lookup"><span data-stu-id="fe234-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="fe234-124">下一 [步：步驟5。將指標儲存至篩選準則](step-5--store-a-pointer-to-the-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="fe234-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe234-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fe234-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe234-126">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="fe234-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



