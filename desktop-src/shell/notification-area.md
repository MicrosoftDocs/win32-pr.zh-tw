---
description: 通知區域是工作列的一部分，可提供通知和狀態的暫時來源。
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: 通知和通知區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318632"
---
# <a name="notifications-and-the-notification-area"></a>通知和通知區域

通知區域是工作列的一部分，可提供通知和狀態的暫時來源。 它也可以用來顯示桌上型電腦上沒有存在的系統和程式功能圖示，例如電池計量、音量控制和網路狀態。 過去已經知道通知區域是系統匣或狀態欄。

本主題包含下列幾節：

-   [通知和通知區域指導方針](#notification-and-notification-area-guidelines)
-   [建立與顯示通知](#notifications-and-the-notification-area)
    -   [新增通知圖示](#add-a-notification-icon)
    -   [定義 NOTIFYICONDATA 版本](#define-the-notifyicondata-version)
    -   [定義通知的外觀和內容](#define-the-notification-look-and-contents)
    -   [檢查使用者狀態](#check-the-user-status)
    -   [顯示通知](#display-the-notification)
    -   [移除圖示](#removing-an-icon)
-   [SDK 範例](#sdk-sample)
-   [相關主題](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a>通知和通知區域指導方針

請參閱 Windows 使用者經驗互動指導方針的 [通知](../uxguide/mess-notif.md) 和 [通知區域](../uxguide/winenv-notification.md) 章節，以取得使用通知和通知區域的最佳做法。 其目標是透過適當的通知使用來提供使用者權益，而不會干擾或困擾。

通知區域不適用於必須立即採取動作的重要資訊。 它也不適合快速程式或命令存取。 從 Windows 7，大部分的功能都是透過應用程式的工作列按鈕來完成。

Windows 7 可讓使用者從應用程式隱藏所有的通知（如果他們選擇的話），因此，您可以使用更好的通知設計和使用方式，讓您的應用程式繼續顯示。 通知會中斷;請確定這是值得的。

Windows 7 引進了「安靜時間」的概念。 當新的使用者第一次登入其帳戶之後，或在作業系統升級或全新安裝之後第一次登入其帳戶時，會定義無訊息時間。 這段時間是為了讓使用者能夠探索並熟悉新環境，而不受通知干擾。 在這段期間內，不應該傳送或顯示大部分的通知。 例外狀況包括使用者預期會看到的意見反應，以回應使用者動作，例如，當使用者插入 USB 裝置或列印檔案時。 本主題稍後會討論關於靜音時間的 API 細節。

## <a name="creating-and-displaying-a-notification"></a>建立與顯示通知

本主題的其餘章節將概述在向使用者顯示應用程式的通知時，所要遵循的基本步驟。

1.  [新增通知圖示](#add-a-notification-icon)
2.  [定義 NOTIFYICONDATA 版本](#define-the-notifyicondata-version)
3.  [定義通知的外觀和內容](#define-the-notification-look-and-contents)
4.  [檢查使用者狀態](#check-the-user-status)
5.  [顯示通知](#display-the-notification)
6.  [移除圖示](#removing-an-icon)

### <a name="add-a-notification-icon"></a>新增通知圖示

若要顯示通知，您必須在通知區域中有一個圖示。 在某些情況下（例如 Microsoft Communicator 或電池計量），該圖示將已存在。 不過，在其他許多情況下，您只需在顯示通知所需的時間內，才將圖示新增至通知區域。 無論是哪一種情況，都是使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 函式來完成。 **Shell \_NotifyIcon** 可讓您新增、修改或刪除通知區域中的圖示。

![包含三個圖示的通知區域](images/taskbar/notificationareaicons.png)

將圖示新增至 Windows 7 的通知區域時，預設會將它新增至通知區域的溢位區段。 此區域包含作用中，但不會顯示在通知區域中的通知區域圖示。 只有使用者可以將溢出的圖示升階到通知區域，不過在某些情況下，系統可以暫時將圖示升階到通知區域中，做為一分鐘) 的簡短預覽 (。

> [!Note]  
> 使用者應該要知道他們想要在其通知區域中看到的圖示。 在通知區域中安裝非暫時性的圖示之前，應該先要求使用者提供許可權。 您也應該提供選項 (一般，雖然它的快捷方式功能表) 從通知區域移除圖示。

 

在 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的呼叫中傳送的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構包含指定通知區域圖示和通知本身的資訊。 以下是通知區域圖示本身特定的專案，可透過 **NOTIFYICONDATA** 設定。

-   從中取得圖示的資源。
-   圖示的唯一識別碼。
-   圖示工具提示的樣式。
-   圖示的狀態 (隱藏、共用或在通知區域中) 。
-   與圖示相關聯之應用程式視窗的控制碼。
-   回呼訊息識別碼，可讓圖示與相關聯的應用程式視窗溝通出現在圖示周框矩形和氣球通知內的事件。 您可以透過 [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)來取出圖示的周框。

您可以透過兩種方式識別通知區域中的每個圖示：

-   在登錄中宣告圖示的 GUID。 這是 Windows 7 和更新版本的慣用方法。
-   與通知區域圖示相關聯的視窗控制碼，加上應用程式定義的圖示識別碼。 這個方法是在 Windows Vista 及更早版本上使用。

通知區域中的圖示可以有工具提示。 工具提示可以是標準工具提示 (慣用的) 或應用程式繪製的彈出 UI。 雖然不需要工具提示，但建議您這樣做。

通知區域圖示應為高 DPI 感知。 應用程式應該在其資源檔中提供16x16 圖元圖示和32x32 圖示，然後使用 [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) 來確保正確載入正確的圖示，並適當地進行調整。

負責通知區域圖標的應用程式應該處理滑鼠按一下圖示。 當使用者以滑鼠右鍵按一下圖示時，應該會顯示一般的快捷方式功能表。 不過，使用滑鼠左鍵按一下滑鼠左鍵的結果會與圖示的功能不同。 它應該會顯示使用者預期會在最適合該內容的表單中看到的內容，也就是快顯視窗、對話方塊或程式視窗本身。 例如，它可以顯示狀態圖示的狀態文字，或是音量控制項的滑杆。

從按一下所產生的快顯視窗或對話方塊的位置，應該放在通知區域中按一下的座標附近。 使用 [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) 來判斷它的位置。

您可以將圖示新增至通知區域，而不會顯示通知，方法是只定義上述 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (圖示特定的成員) 和呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，如下所示：


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



您也可以將圖示新增至通知區域，並在一次呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)時顯示通知。 若要這樣做，請繼續進行本主題中的指示。

### <a name="define-the-notifyicondata-version"></a>定義 NOTIFYICONDATA 版本

隨著 Windows 的進展， [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 結構已經擴充，以包含更多成員來定義更多功能。 常數用來宣告要搭配您的通知區域圖示使用的 **NOTIFYICONDATA** 版本，以允許回溯相容性。 除非有令人信服的理由，否則強烈建議您使用 \_ \_ Windows Vista 中引進的 NOTIFYICON 第4版。 此版本提供完整的可用功能，包括慣用的功能，可透過已註冊的 GUID 來識別通知區域圖示、絕佳的回呼機制，以及更好的協助工具。

透過下列呼叫設定版本：


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



請注意，這個 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 呼叫不會顯示通知。

### <a name="define-the-notification-look-and-contents"></a>定義通知的外觀和內容

通知是一種特殊類型的氣球工具提示控制項。 它包含標題、主體文字和圖示。 就像視窗一樣，它的右上角有一個 [ **關閉** ] 按鈕。 它也包含一個 [ **選項** ] 按鈕，可開啟主控台中的通知區域圖示專案，讓使用者可以顯示或隱藏圖示，或只顯示沒有圖示的通知。

![通知氣球的螢幕擷取畫面，指出電池電力偏低](images/taskbar/notificationballoon.png)

在 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的呼叫中傳送的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構包含同時指定通知區域圖示和通知氣球本身的資訊。 以下是可透過 **NOTIFYICONDATA** 設定的通知特定專案。

-   要在通知氣球中顯示的圖示，由通知類型指定。 您可以指定圖示的大小，也可以指定自訂圖示。
-   通知標題。 在英文 (中，此標題的長度上限為48個字元，以容納當地語系化) 。 標題是通知的第一行，而且會透過使用字型大小、色彩和權數來分開設定。
-   要在通知主體中使用的文字。 此文字最多可有200個字元的英文 (，以配合當地語系化) 。
-   如果通知無法立即顯示，是否應捨棄通知。
-   通知的超時時間。 在 Windows Vista 和更新版本的系統中，會忽略這項設定，以改用整個系統的協助工具超時設定。
-   通知是否應遵守無訊息時間，請透過 [**NIIF 尊重無訊息 \_ \_ \_ 時間**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 旗標來設定。

> [!Note]  
> [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)和 [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)介面是 [**Shell \_ NOTIFYICON**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的元件物件模型 (COM) 包裝函式。 不過，目前無法 \_ \_ 直接透過 **Shell \_ NOTIFYICON** 提供完整的 NOTIFYICON 第4版功能，包括使用 GUID 來識別通知區域圖示。

 

### <a name="check-the-user-status"></a>檢查使用者狀態

系統使用 [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) 函式來檢查使用者是否處於無訊息時間、離開電腦，或處於不間斷的狀態，例如展示模式。 系統是否會顯示您的通知取決於此狀態。

> [!Note]  
> 如果您的應用程式使用未使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)、 [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)或 [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)的自訂通知方法，則應該一律明確地呼叫 [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) ，以判斷是否應該在該時間顯示通知 UI。

 

當使用者離開時傳送的通知已排入佇列以供顯示，但因為您無法得知使用者將會傳回的時間，或是在該時間之後是否仍然有效通知，您可能會考慮稍後再重新傳送通知。

Unshown 時，會捨棄在無訊息期間傳送的通知。 設計指導方針會要求所有通知都可忽略。 它們應該不需要立即的使用者動作。 因此，沒有任何通知應該覆寫無訊息時間。

### <a name="display-the-notification"></a>顯示通知

設定 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 版本並在 **NOTIFYICONDATA** 結構中定義通知之後，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來顯示圖示。

-   如果沒有通知區域圖示，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來新增圖示。 針對暫時性和非暫時性的圖示進行這項作業。
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   如果通知區域圖示已經存在，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來修改圖示。
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

下列程式碼顯示設定 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 資料並透過 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)傳送它的範例。 請注意，此範例會透過 Windows 7) 中偏好的 GUID (來識別通知圖示。


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a>移除圖示

若要移除圖示，例如，當您只是暫時新增圖示來廣播通知時，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)，如下所示。 此呼叫只需要最基本的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 結構來識別圖示。


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> 卸載應用程式時，它的通知區域圖示仍然可以在主控台的 [通知區域圖示] 頁面中，以選項的形式出現在最多七天。 不過，任何進行的變更都不會有任何作用。

 

## <a name="sdk-sample"></a>SDK 範例

如需使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的完整範例，請參閱 Windows 軟體開發套件 (SDK) 中的 [NotificationIcon 範例](samples-notificationicon.md)範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[工作列](taskbar.md)
</dt> <dt>

[工作列擴充功能](taskbar-extensions.md)
</dt> </dl>

 

 
