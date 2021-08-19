---
title: 嚴格合規性
description: 當您啟用 STRICT 類型檢查時，會成功編譯的部分原始程式碼可能會產生錯誤訊息。
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29baee071bd8d7c236ec5f2f99d1dff11aeac37deb44b0d8a6254325c9a75df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928143"
---
# <a name="strict-compliance"></a>嚴格合規性

當您啟用 **STRICT** 類型檢查時，會成功編譯的部分原始程式碼可能會產生錯誤訊息。 下列各節說明在啟用 **STRICT** 時進行程式碼編譯的基本需求。 建議執行其他步驟，尤其是為了產生可移植的程式碼。

## <a name="general-requirements"></a>一般需求

主要需求是您必須宣告正確的控制碼類型和函式指標，而不是依賴更多一般類型。 您無法使用另一個需要的控制碼類型。 這也表示您可能必須變更函式宣告，並使用更多型別轉換。

為了獲得最佳結果，只有在必要時才使用泛型 **控制碼** 類型。

## <a name="declaring-functions-within-your-application"></a>在您的應用程式中宣告函數

確定已宣告所有的應用程式函數。 建議將所有函式宣告放在 include 檔案中，因為您可以輕鬆地掃描您的宣告，並尋找應變更的參數和傳回類型。

如果您使用 **/Zg** 編譯器選項來建立函式的標頭檔，請記住，您將會根據您是否已啟用 **STRICT** 型別檢查來取得不同的結果。 在 **STRICT** 停用的情況下，所有的控制碼類型都會產生相同的基底類型。 在 **STRICT** 啟用的情況下，它們會產生不同的基底類型。 若要避免發生衝突，您必須在每次啟用或停用 **STRICT** 時重新建立標頭檔，或編輯標頭檔以使用類型 **HWND**、 **HDC**、 **控制碼** 等，而不是基底類型。

您從 Windows 複製到原始程式碼的任何函式宣告可能已變更，而您的本機宣告可能已過期。 移除本機宣告。

## <a name="types-that-require-casts"></a>需要轉換的類型

某些函式具有泛型傳回類型或參數。 例如，視內容而定， [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式會傳回可能任意數目之類型的資料。 當您在原始程式碼中看到任何這些函式時，請確定您使用正確的型別轉換，而且它盡可能明確。 下列清單是這些函數的範例。

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

當您呼叫 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)、 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)或 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)時，應該先將結果轉換成 **UINT \_ 指標** 類型。 針對傳回 **LRESULT** 或 **LONG \_ PTR** 值的任何函式，您必須採取類似的步驟，其中結果包含控制碼。 這是撰寫可移植程式碼的必要項，因為控制碼的大小會隨著 Windows 的版本而有所不同。  (**UINT \_ PTR**) 轉換可確保正確的轉換。 下列程式碼顯示 **SendMessage** 將控制碼傳回給筆刷的範例：


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



[ **CreateWindow** ] 和 [ **CreateWindowEx** ] 參數 *hmenu* 有時會用來傳遞整數控制項識別碼 (識別碼) 。 在此情況下，您必須將識別碼轉換成 **HMENU** 型別：


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>其他考量

若要充分利用 **嚴格** 的型別檢查，您應該遵循其他指導方針。 如果您進行下列變更，您的程式碼將會在未來版本的 Windows 中更容易移植。

**WPARAM**、 **LPARAM**、 **LRESULT** 和 **LPVOID** 類型都是多型 *資料類型*。 它們會在不同的時間保存不同類型的資料，即使已啟用 **STRICT** 型別檢查也是一樣。 若要取得類型檢查的優點，您應該儘快轉換這些類型的值。  (請注意，message crackers 會以可移植的方式自動為您重新轉換 *wParam* 和 *lParam* ) 。

請特別小心區別 **HMODULE** 和 **HINSTANCE** 類型。 即使已啟用 **STRICT** ，它們也會定義為相同的基底類型。 大部分的核心模組管理函式都會使用 **HINSTANCE** 類型，但有一些函數會傳回或只接受 **HMODULE** 類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[停用 STRICT](disabling-strict.md)
</dt> <dt>

[啟用 STRICT](enabling-strict.md)
</dt> </dl>

 

 