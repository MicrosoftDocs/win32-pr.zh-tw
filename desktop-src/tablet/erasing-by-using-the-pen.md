---
description: 如果您選擇在應用程式中使用 InkOverlay 物件來執行清除，您可以使用下列兩種方法的其中一種來執行此動作。
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: 使用畫筆進行清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386155"
---
# <a name="erasing-by-using-the-pen"></a><span data-ttu-id="491dd-103">使用畫筆進行清除</span><span class="sxs-lookup"><span data-stu-id="491dd-103">Erasing by Using the Pen</span></span>

<span data-ttu-id="491dd-104">如果您選擇在應用程式中使用 [**InkOverlay**](inkoverlay-class.md) 物件來執行清除，您可以使用下列兩種方法的其中一種來執行此動作。</span><span class="sxs-lookup"><span data-stu-id="491dd-104">If you choose to implement erasing in your application other than by using the [**InkOverlay**](inkoverlay-class.md) object, you can do so by using one of the following two methods.</span></span>

## <a name="using-the-tip-of-the-pen"></a><span data-ttu-id="491dd-105">使用畫筆的秘訣</span><span class="sxs-lookup"><span data-stu-id="491dd-105">Using the Tip of the Pen</span></span>

<span data-ttu-id="491dd-106">Tablet 畫筆的秘訣通常用於手寫和繪圖;不過，秘訣也可以用來清除筆墨。</span><span class="sxs-lookup"><span data-stu-id="491dd-106">The tip of the tablet pen is generally used for handwriting and drawing; however, the tip can also be used to erase ink.</span></span> <span data-ttu-id="491dd-107">若要這樣做，應用程式必須具有使用者可以採用的清除模式。</span><span class="sxs-lookup"><span data-stu-id="491dd-107">To do so, the application must have an erase mode that users can employ.</span></span> <span data-ttu-id="491dd-108">在此模式中，請使用點擊測試來判斷游標要移動的筆跡。</span><span class="sxs-lookup"><span data-stu-id="491dd-108">In this mode, use hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="491dd-109">您可以將清除模式設定為只刪除游標所傳遞的筆墨，或只刪除與資料指標路徑相交的整個筆劃，視設計或功能考慮而定。</span><span class="sxs-lookup"><span data-stu-id="491dd-109">You can set the erase mode to delete only the ink that the cursor passes over or whole strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="491dd-110">如需如何使用清除模式來清除筆墨的範例，請參閱 [筆墨清除範例](ink-erasing-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="491dd-110">For an example of how to use an erase mode to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

## <a name="using-the-top-of-the-pen"></a><span data-ttu-id="491dd-111">使用畫筆的頂端</span><span class="sxs-lookup"><span data-stu-id="491dd-111">Using the Top of the Pen</span></span>

<span data-ttu-id="491dd-112">若要在 tablet 畫筆上方執行清除，您的應用程式必須在游標處尋找變更。</span><span class="sxs-lookup"><span data-stu-id="491dd-112">To implement erasing with the top of the tablet pen, your application must look for a change in the cursor.</span></span> <span data-ttu-id="491dd-113">若要尋找反向資料指標，請接聽 [**CursorInRange**](inkoverlay-cursorinrange.md) 事件，以判斷游標在應用程式內容中的時間。</span><span class="sxs-lookup"><span data-stu-id="491dd-113">To look for the inverted cursor, listen for the [**CursorInRange**](inkoverlay-cursorinrange.md) event to determine when the cursor is within the context of your application.</span></span> <span data-ttu-id="491dd-114">當資料指標在範圍內時，請在資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件上尋找 [**反向**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted)屬性。</span><span class="sxs-lookup"><span data-stu-id="491dd-114">When the cursor is in range, look for the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span> <span data-ttu-id="491dd-115">如果 **反向** 屬性為 **true**，請執行點擊測試來判斷游標要移動的筆墨。</span><span class="sxs-lookup"><span data-stu-id="491dd-115">If the **Inverted** property is **true**, perform hit testing to determine which ink the cursor is moving over.</span></span> <span data-ttu-id="491dd-116">根據設計或功能考慮，清除與游標路徑相交的筆墨或筆觸。</span><span class="sxs-lookup"><span data-stu-id="491dd-116">Erase either the ink or the strokes that intersect the path of the cursor, depending upon design or functional considerations.</span></span>

<span data-ttu-id="491dd-117">如需如何使用畫筆頂端來清除筆墨的範例，請參閱 [筆墨清除範例](ink-erasing-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="491dd-117">For an example of how to use the top of the pen to erase ink, see the [Ink Erasing Sample](ink-erasing-sample.md).</span></span>

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a><span data-ttu-id="491dd-118">判斷是否已啟用在畫筆上方清除</span><span class="sxs-lookup"><span data-stu-id="491dd-118">Determining if Erasing with the Top of the Pen Is Enabled</span></span>

<span data-ttu-id="491dd-119">使用者可以使用畫筆的上方來清除針對 Tablet PC 所設計之應用程式中的筆跡（如果其特定硬體允許的話）。</span><span class="sxs-lookup"><span data-stu-id="491dd-119">Users can use the top of the pen to erase ink in applications designed for Tablet PC, if their particular hardware allows for it.</span></span> <span data-ttu-id="491dd-120">這項功能是由 [Tablet 和畫筆設定] 控制台對話方塊中 [畫筆選項] 索引標籤上的 [畫筆按鈕] 群組方塊中的核取方塊來存取。</span><span class="sxs-lookup"><span data-stu-id="491dd-120">This functionality is accessed by a check box in the Pen buttons group box on the Pen Options tab of the Tablet and Pen Settings control panel dialog.</span></span> <span data-ttu-id="491dd-121">若要偵測使用者是否已在畫筆上方啟用清除，請檢查下列登錄子機碼：</span><span class="sxs-lookup"><span data-stu-id="491dd-121">To detect if the user has enabled erasing for the top of the pen, check the following registry subkey:</span></span>

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

<span data-ttu-id="491dd-122">此子機碼的 `EraseEnable` 專案類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="491dd-122">The `EraseEnable` entry of this subkey is of type **REG\_DWORD**.</span></span> <span data-ttu-id="491dd-123">此專案的值為1表示已啟用，或0表示停用。</span><span class="sxs-lookup"><span data-stu-id="491dd-123">The value of this entry is 1 for enabled, or 0 for disabled.</span></span> <span data-ttu-id="491dd-124">保留其他值供以後使用。</span><span class="sxs-lookup"><span data-stu-id="491dd-124">Other values are reserved for future use.</span></span>

<span data-ttu-id="491dd-125">如果您的應用程式允許使用畫筆的頂端進行清除，您應該在下列情況下檢查並快取 EraseEnable 專案的值：</span><span class="sxs-lookup"><span data-stu-id="491dd-125">If your application allows the top of the pen to be used for erasing, you should check and cache the value of the EraseEnable entry when:</span></span>

-   <span data-ttu-id="491dd-126">您的應用程式隨即啟動。</span><span class="sxs-lookup"><span data-stu-id="491dd-126">Your application launches.</span></span>
-   <span data-ttu-id="491dd-127">任何時候您的應用程式在失去焦點之後都會收到焦點。</span><span class="sxs-lookup"><span data-stu-id="491dd-127">Any time your application receives focus after losing focus.</span></span>

<span data-ttu-id="491dd-128">使用這個快取的值來適當地修改應用程式的行為。</span><span class="sxs-lookup"><span data-stu-id="491dd-128">Use this cached value to modify the behavior of your application appropriately.</span></span>

<span data-ttu-id="491dd-129">下列 C \# 範例會定義檢查子機碼 `GetEraseEnabled` 專案值的方法 `EraseEnable` `SysEventParameters` 。</span><span class="sxs-lookup"><span data-stu-id="491dd-129">The following C\# example defines a `GetEraseEnabled` method that checks the value of the `EraseEnable` entry of the `SysEventParameters` subkey.</span></span> <span data-ttu-id="491dd-130">如果專案的值為1，則此 `GetEraseEnabled` 方法會傳回 **TRUE** ; 如果專案的值為0，則會傳回 **FALSE** ; 如果專案的值不是1或0，則會擲回 [InvalidOperationException](/dotnet/api/system.invalidoperationexception) 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="491dd-130">The `GetEraseEnabled` method returns **TRUE** if the value of the entry is 1; returns **FALSE** if the value of the entry is 0; or throws an [InvalidOperationException](/dotnet/api/system.invalidoperationexception) exception if the value of the entry is other than 1 or 0.</span></span> <span data-ttu-id="491dd-131">如果子機碼 `GetEraseEnabled` 或專案不存在，此方法會傳回 **TRUE** 的預期值。</span><span class="sxs-lookup"><span data-stu-id="491dd-131">The `GetEraseEnabled` method returns the expected value of **TRUE** if either the subkey or the entry is not present.</span></span>


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
