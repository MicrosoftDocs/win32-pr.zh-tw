---
description: 如果您選擇在應用程式中使用 InkOverlay 物件來執行清除，您可以使用下列兩種方法的其中一種來執行此動作。
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: 使用畫筆進行清除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96d7d281f4e94a4a53f7e99e83c38192ceb7d31fbf9ee643653a20b4836a7cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936568"
---
# <a name="erasing-by-using-the-pen"></a>使用畫筆進行清除

如果您選擇在應用程式中使用 [**InkOverlay**](inkoverlay-class.md) 物件來執行清除，您可以使用下列兩種方法的其中一種來執行此動作。

## <a name="using-the-tip-of-the-pen"></a>使用畫筆的秘訣

Tablet 畫筆的秘訣通常用於手寫和繪圖;不過，秘訣也可以用來清除筆墨。 若要這樣做，應用程式必須具有使用者可以採用的清除模式。 在此模式中，請使用點擊測試來判斷游標要移動的筆跡。 您可以將清除模式設定為只刪除游標所傳遞的筆墨，或只刪除與資料指標路徑相交的整個筆劃，視設計或功能考慮而定。

如需如何使用清除模式來清除筆墨的範例，請參閱 [筆墨清除範例](ink-erasing-sample.md)。

## <a name="using-the-top-of-the-pen"></a>使用畫筆的頂端

若要在 tablet 畫筆上方執行清除，您的應用程式必須在游標處尋找變更。 若要尋找反向資料指標，請接聽 [**CursorInRange**](inkoverlay-cursorinrange.md) 事件，以判斷游標在應用程式內容中的時間。 當資料指標在範圍內時，請在資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件上尋找 [**反向**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted)屬性。 如果 **反向** 屬性為 **true**，請執行點擊測試來判斷游標要移動的筆墨。 根據設計或功能考慮，清除與游標路徑相交的筆墨或筆觸。

如需如何使用畫筆頂端來清除筆墨的範例，請參閱 [筆墨清除範例](ink-erasing-sample.md)。

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>判斷是否已啟用在畫筆上方清除

使用者可以使用畫筆的上方來清除針對 Tablet PC 所設計之應用程式中的筆跡（如果其特定硬體允許的話）。 這項功能是由 Tablet 和 Pen 設定 [控制台] 對話方塊之 [畫筆選項] 索引標籤上的 [畫筆按鈕] 群組方塊中的核取方塊所存取。 若要偵測使用者是否已在畫筆上方啟用清除，請檢查下列登錄子機碼：

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

此子機碼的 `EraseEnable` 專案類型為 **REG \_ DWORD**。 此專案的值為1表示已啟用，或0表示停用。 保留其他值供以後使用。

如果您的應用程式允許使用畫筆的頂端進行清除，您應該在下列情況下檢查並快取 EraseEnable 專案的值：

-   您的應用程式隨即啟動。
-   任何時候您的應用程式在失去焦點之後都會收到焦點。

使用這個快取的值來適當地修改應用程式的行為。

下列 C \# 範例會定義檢查子機碼 `GetEraseEnabled` 專案值的方法 `EraseEnable` `SysEventParameters` 。 如果專案的值為1，則此 `GetEraseEnabled` 方法會傳回 **TRUE** ; 如果專案的值為0，則會傳回 **FALSE** ; 如果專案的值不是1或0，則會擲回 [InvalidOperationException](/dotnet/api/system.invalidoperationexception) 例外狀況。 如果子機碼 `GetEraseEnabled` 或專案不存在，此方法會傳回 **TRUE** 的預期值。


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



 

 
