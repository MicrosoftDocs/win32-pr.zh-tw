---
description: 在許多情況下，自動安裝可能需要暫時或持續停用。
ms.assetid: 5e65a3d8-04b9-46ba-b4e5-a976e1923bfd
title: 啟用和停用自動啟動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd14a1dfd3aadb94f3586dec783ea6d394f717f500b5ac103c65fcb813baf14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090778"
---
# <a name="enabling-and-disabling-autorun"></a>啟用和停用自動啟動

在許多情況下，自動安裝可能需要暫時或持續停用。 例如，自動執行可能會干擾正在執行之應用程式的作業，而且必須在持續期間內停用。 系統提供數種方式來停用自動運行。

-   [以程式設計方式隱藏自動運行](#suppressing-autorun-programmatically)
-   [使用登錄來停用自動播放](#using-the-registry-to-disable-autorun)
-   [其他類型儲存體媒體的自動運行](#autorun-for-other-types-of-storage-media)

## <a name="suppressing-autorun-programmatically"></a>以程式設計方式隱藏自動運行

有許多情況下，可能需要以程式設計的方式隱藏自動安裝。 以下為兩個範例：

-   您的應用程式有一個安裝程式，要求使用者插入另一個可能包含自動播放 .inf 檔案的光碟片。
-   在應用程式的作業期間，使用者可能需要插入另一張可能包含自動執行 .inf 檔案的光碟片。

在任一種情況下，您通常不會想要在原始進行中時啟動另一個應用程式。

使用者可以在插入 cd-rom 時按住 SHIFT 鍵，以手動隱藏自動安裝。 不過，通常最好是以程式設計方式處理這項作業，而不是根據使用者。

使用具有 Shell [4.70 版](versions.md)和更新版本的系統，Windows 將 "QueryCancelAutoPlay" 訊息傳送到前景視窗。 您的應用程式可以回應此訊息以抑制自動運行。 這種方法是由系統公用程式（例如 [ [開啟](../dlgbox/open-and-save-as-dialog-boxes.md) 一般] 對話方塊）用來停用自動運行。

下列程式碼片段說明如何設定和處理此訊息。 您的應用程式必須在前景視窗中執行。 首先，將 "QueryCancelAutoPlay" 註冊為 Windows 訊息：


```C++
uMessage = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
```



您應用程式的視窗必須在前景才能接收此訊息。 訊息處理常式應該會傳回 **TRUE** 以取消自動運行，並傳回 **FALSE** 來啟用它。 下列程式碼片段說明如何使用此訊息來停用自動執行。


```C++
UINT g_uQueryCancelAutoPlay = 0;

LRESULT WndProc(HWND hwnd, UINT uMsg,  WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ... 
    default: 
        if (!g_uQueryCancelAutoPlay)
        { 
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg && uMsg == g_uQueryCancelAutoPlay)
        { 
            return TRUE;       // Cancel AutoRun
        }
    }
}
```



如果您的應用程式使用對話方塊，而且必須回應 "QueryCancelAutoPlay" 訊息，則不會直接傳回 **TRUE** 或 **FALSE**。 請改為呼叫 [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ，並將 *NIndex* 設定為 **DWL \_ MSGRESULT**。 將 *dwNewLong* 參數設定為 **TRUE** 以取消自動啟動，並將 FALSE 設定為 **FALSE** 。 例如，下列範例對話方塊程式會在收到「QueryCancelAutoPlay」訊息時，取消自動執行。


```C++
UINT g_uQueryCancelAutoPlay = 0;

BOOL DialogProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (uMsg) 
    { 
    ...
    default: 
        if (!g_uQueryCancelAutoPlay)
        {
            g_uQueryCancelAutoPlay = RegisterWindowMessage(TEXT("QueryCancelAutoPlay"));
        } 
        if (uMsg == g_uQueryCancelAutoPlay) 
        {
            SetWindowLong(hDlg, DWL_MSGRESULT, TRUE);          
            return 1;               
        }
    } 
```



## <a name="using-the-registry-to-disable-autorun"></a>使用登錄來停用自動播放

有兩個可用來持續停用自動執行的登錄值： NoDriveAutoRun 和 NoDriveTypeAutoRun。 第一個值會停用指定磁碟機號的自動運行，而第二個值會停用磁片磁碟機類別的自動運行。 如果其中一個值設定為停用特定裝置的自動安裝，則會停用。 如需停用自動播放功能的詳細資訊，請參閱知識庫文章[如何停用 Windows 中的自動運行功能](https://support.microsoft.com/kb/967715)。 本文列出您必須安裝才能正確停用自動播放功能的不同更新。

> [!Note]  
> NoDriveAutoRun 和 NoDriveTypeAutoRun 值只能由系統管理員修改，以變更整個系統的值，以供測試或管理之用。 應用程式不應該修改這些值，因為無法將它們可靠地還原為其原始值。

 

NoDriveAutoRun 值會停用指定磁碟機號的自動運行。 它是登錄 \_ 的 DWORD 資料值，可在下列機碼下找到：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

值的第一個位對應到磁片磁碟機 A：，第二個是 B：，依此類推。 若要停用一或多個磁碟機號的自動播放，請設定對應的位。 例如，若要停用 A：和 C：磁片磁碟機，請將 NoDriveAutoRun 設定為 `0x00000005` 。

NoDriveTypeAutoRun 值會停用磁片磁碟機類別的自動運行。 它是登錄 \_ DWORD 或4位元組的 reg \_ 二進位資料值，可在相同的索引鍵下找到。

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
```

藉由設定此值的第一個位元組的位，可以排除不同的磁片磁碟機，而不使用自動執行。

下表提供位和位元遮罩常數，可在 NoDriveTypeAutoRun 的第一個位元組中設定，以停用特定磁片磁碟機類型的自動執行。 您必須重新開機 Windows 檔案總管，變更才會生效。



| 位數位 | 位元遮罩常數      | Description                                             |
|------------|-----------------------|---------------------------------------------------------|
| 0x04       | **磁片磁碟機 \_ 可移動** | 磁片可以從磁片磁碟機 (（例如磁片) ）移除。 |
| 0x08       | **磁片磁碟機 \_ 修正**      | 無法從磁片磁碟機 (硬碟) 中移除磁片。        |
| 0x10       | **遠端磁片磁碟機 \_**     | 網路磁碟機機。                                          |
| 0x20       | **光碟機 \_ 磁片磁碟機**      | CD-ROM 光碟機。                                           |
| 0x40       | **驅動 \_ RAMDISK**    | RAM 磁碟。                                               |



 

## <a name="autorun-for-other-types-of-storage-media"></a>其他類型儲存體媒體的自動運行

自動執行主要是用來在 CD-ROM 和 DVD-ROM 上將應用程式公開散發，而且不建議將其用於其他儲存體媒體。 不過，在其他類型的卸除式存放裝置媒體上啟用自動啟動通常會很有用。 這項功能通常是用來簡化自動播放 .inf 檔案的偵錯工具。 當符合下列準則時，自動執行只適用于卸除式存放裝置裝置：

-   裝置必須具有自動運行時相容的驅動程式。 若要與自動相容，驅動程式必須透過傳送 [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) 訊息，通知系統已插入磁片。
-   插入之媒體的根目錄必須包含自動運行的 .inf 檔案。
-   裝置不能透過登錄停用自動執行[。](#using-the-registry-to-disable-autorun)
-   前景應用程式未 [隱藏](#suppressing-autorun-programmatically) 自動運行。

> [!Note]  
> 這項功能不應用來將應用程式散發至卸載式媒體。 由於在卸載式媒體上執行自動執行可提供簡單的方式來散佈電腦病毒，因此使用者應該會懷疑包含自動執行 .inf 檔案的任何公開分散式磁片磁碟機。

 

通常，自動啟動會自動啟動，但也可以手動啟動。 如果裝置符合上面所列的條件，磁碟機號的快捷方式功能表就會包含 [ **自動播放** ] 命令。 若要手動執行自動執行，請在磁片磁碟機圖示上按一下滑鼠右鍵，然後從快捷方式功能表選取 [ **自動播放** ]，或按兩下磁片磁碟機圖示。 如果驅動程式不相容，則快捷方式功能表將不會有 [ **自動播放** ] 專案，而且無法啟動自動啟動。

自動運行時相容的驅動程式會隨附于一些卸載式磁片磁碟機，以及一些其他類型的卸載式媒體，例如 CompactFlash 卡。 自動播放也適用于對應至磁碟機號 Windows 檔案總管的網路磁碟機機，或透過[Microsoft Management Console (MMC) ](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)掛接。 如同掛接的硬體一樣，掛接的網路磁碟機機在其根目錄中必須有執行中的 .inf 檔案，而且不得透過登錄來停[用。](#using-the-registry-to-disable-autorun)

 

 
