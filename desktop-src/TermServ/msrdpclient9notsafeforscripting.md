---
title: MsRdpClient9NotSafeForScripting 類別
description: Microsoft RDP 用戶端控制-第10版。
ms.assetid: 6F782984-1A17-449E-958F-EF887C340C49
ms.tgt_platform: multiple
keywords:
- MsRdpClient9NotSafeForScripting 類別遠端桌面服務
- MsRdpClient9NotSafeForScripting 類別遠端桌面服務，說明
topic_type:
- apiref
api_name:
- MsRdpClient9NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da0e33738026a1a1f22cd1d535a2d78fa382f8a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480654"
---
# <a name="msrdpclient9notsafeforscripting-class"></a>MsRdpClient9NotSafeForScripting 類別

Microsoft RDP 用戶端控制-第10版

這個類別會執行下列介面。

-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)
-   [**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)

**MsRdpClient9NotSafeForScripting** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MsRdpClient9NotSafeForScripting** 類別有這些方法。



| 方法                                                                                      | 描述                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                            | 附加事件。 <br/>                                                                                                                                                                                                                                                                |
| [**連線**](imstscax-connect.md)                                                         | 使用目前在控制項上設定的屬性起始連接。<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。<br/>                                                                                                                                                                                              |
| [**Vemap.detachevent**](imsrdpclient9-detachevent.md)                                            | 卸離事件。 <br/>                                                                                                                                                                                                                                                                |
| [**中斷連線**](imstscax-disconnect.md)                                                   | 中斷使用中連接。<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | 捕獲錯誤碼和錯誤訊息。<br/>                                                                                                                                                                                                                                      |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                                        | 抓取指定狀態碼的狀態文字。<br/>                                                                                                                                                                                                                           |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | 抓取為虛擬通道設定的選項。<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | 通知遠端桌面的裝置重新導向模組，ActiveX 控制系統上的裝置變更已發生。 這個方法會將 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 通知傳遞給控制項。<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | 在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | 在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，[憑證錯誤] 對話方塊) 。<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | 當用戶端控制項自動重新連接到遠端會話時呼叫。<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | 當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | 當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | 當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | 當用戶端呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時呼叫。<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | 當用戶端控制項正在建立與 RD 工作階段主機 server 的連接時呼叫。<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | 當用戶端控制項開始連接到伺服器以回應 [**IMsTscAx：：連線**](imstscax-connect.md)的呼叫時呼叫。<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | 當使用者在連接列上向下拖曳時呼叫。<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | 當按下連接列中的 [裝置] 按鈕時呼叫。<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | 當用戶端控制項與 RD 工作階段主機伺服器中斷連線時呼叫。<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | 當用戶端進入全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | 當用戶端控制項遇到嚴重錯誤時呼叫。<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | 在按下放開焦點按鍵組合時呼叫。 例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | 當使用者在 [**IMsRdpClientAdvancedSettings：:p 長 \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 方法設定期間沒有滑鼠或鍵盤輸入時呼叫。<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | 當用戶端離開全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | 當用戶端控制項成功登入 RD 工作階段主機伺服器時呼叫，並遵循 [Windows 登入] 對話方塊的顯示。<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | 發生登入錯誤或其他登入事件時呼叫。<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | 當滑鼠輸入模式變更時呼叫。<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | 在網路狀態變更時呼叫。<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | 當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。 只有當 **NotifyTSPublicKey** 屬性為 **VARIANT \_ TRUE** 時，才會呼叫此事件。<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | 呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | 在顯示 RemoteApp 程式時呼叫。<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | 當 RemoteApp 程式傳回結果給用戶端控制項時呼叫。<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | 當 RemoteApp 視窗顯示時呼叫。<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | 當使用者在全螢幕模式下的連接列上按下 **最小化** 按鈕時呼叫。 引發此事件是容器應用程式本身最小化的要求。<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | 當用戶端要求切換至全螢幕模式並呼叫 [**IMsTscAdvancedSettings：:p 使用 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 方法時呼叫，以將 **ContainerHandledFullScreen** 屬性設定為非零值。<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | 當用戶端要求離開全螢幕模式，且 [**IMsTscAdvancedSettings：:p 的 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 屬性已設定為非零值時呼叫。<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | 當用戶端收到系統訊息時呼叫。<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | 當控制項取得使用者名稱時呼叫。<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | 當用戶端控制項遇到不嚴重的錯誤狀況時呼叫。<br/>                                                                                                                                                                                                    |
| [**重新連接**](imsrdpclient8-reconnect.md)                                                | 重新連接到具有新桌面寬度和高度的遠端會話。<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | 要求正常關機用戶端控制項。<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | 重設控制項中的所有密碼狀態。<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | 將一連串的按鍵傳送到控制項。 按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | 透過先前使用 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至 RD 工作階段主機伺服器。<br/>                                                                                         |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                                  | 使動作在遠端會話中執行。<br/>                                                                                                                                                                                                                            |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | 設定用戶端控制項的虛擬通道選項。<br/>                                                                                                                                                                                                                           |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)              | 同步處理會話顯示設定。 <br/>                                                                                                                                                                                                                                            |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85))          | 更新會話顯示設定。 <br/>                                                                                                                                                                                                                                                 |



 

### <a name="properties"></a>屬性

**MsRdpClient9NotSafeForScripting** 類別具有這些屬性。




| 屬性 | 存取類型 | Description | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | 唯讀<br /> | <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings</strong></a>介面指標。<br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | 唯讀<br /> | <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | 唯讀<br /> | <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | 唯讀<br /> | <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | 唯讀<br /> | <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a>介面指標。<br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | 唯讀<br /> | 要 <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>的介面。<br /> | 
| <a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br /> | 唯讀<br /> | 要 <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>的介面。<br /> | 
| <a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a><br /> | 唯讀<br /> | 支援 <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> 介面的物件。<br /> | 
| <a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br /> | 唯讀<br /> | 表示 settings 物件的 <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> 介面。<br /> | 
| <a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br /> | 讀取/寫入<br /> | 指定 [認證] 對話方塊是否顯示啟用儲存認證的核取方塊。<br /> | 
| <a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a><br /> | 讀取/寫入<br /> | 指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。<br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | 讀取/寫入<br /> | 不支援這個屬性。<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | 讀取/寫入<br /> | 不支援這個屬性。<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | 唯讀<br /> | 目前控制項的最大加密強度。<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | 唯寫<br /> | 以純文字格式 ActiveX 控制密碼的遠端桌面。<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br /> | 讀取/寫入<br /> | 目前控制項的色彩深度。<br /> | 
| <a href="imstscax-connected.md"><strong>連線</strong></a><br /> | 唯讀<br /> | 目前控制項的連接狀態。<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | 讀取/寫入<br /> | 控制項處於連接狀態時，在控制項的工作區中顯示的文字。<br /> | 
| <a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br /> | 讀取/寫入<br /> | 控制項連接時，顯示在控制項中央的文字。<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | 讀取/寫入<br /> | 要為連接列顯示的文字字串。<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | 讀取/寫入<br /> | 目前的控制項在初始遠端桌面上的高度（以圖元為單位）。<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | 讀取/寫入<br /> | 目前的控制項寬度（以圖元為單位），在初始的遠端桌面。<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | 唯讀<br /> | 可用於重新導向的 PnP 裝置集合。<br /> | 
| <a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a><br /> | 唯寫<br /> | 指定遠端桌面 ActiveX 控制項是否應該停用連接列。<br /> | 
| <a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a><br /> | 讀取/寫入<br /> | 指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | 讀取/寫入<br /> | 在連接結束之前出現在控制項中央的文字。<br /> | 
| <a href="imstscax-domain.md"><strong>域</strong></a><br /> | 讀取/寫入<br /> | 目前使用者登入的網域。<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | 唯讀<br /> | 可用於重新導向的磁片磁碟機集合。<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | 讀取/寫入<br /> | 指定是否啟用此連接的 CredSSP。<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | 唯讀<br /> | 有關用戶端控制項中斷連接原因的詳細資訊。<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br /> | 讀取/寫入<br /> | 指出控制項是否處於全螢幕模式。<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | 唯寫<br /> | 當控制項處於全螢幕模式時，所顯示的視窗標題。<br /> | 
| <a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a><br /> | 唯讀<br /> | 指定遠端監視的周框。<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | 唯讀<br /> | 指出控制項是否已顯示水準捲軸。<br /> | 
| <a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br /> | 讀取/寫入<br /> | 指定使用者是否使用 RD Web 存取介面啟動用戶端控制項。<br /> | 
| <a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br /> | 讀取/寫入<br /> | 指定是否將 RDP 設定標示為安全。<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | 唯讀<br /> | 入口網站啟動器的用戶端設定。<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | 讀取/寫入<br /> | 指定此連接是否支援 NegotiateSecurityLayer 設定。<br /><blockquote>[!Note]<br />當 <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> 已啟用並存在於用戶端上，或當安全通訊端層 (SSL) 啟用使用者驗證時，會忽略 NegotiateSecurityLayer。</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | 讀取/寫入<br /> | 不支援這個屬性。<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | 讀取/寫入<br /> | 不支援這個屬性。<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | 讀取/寫入<br /> | 指定是否應顯示 [提示輸入認證] 對話方塊。<br /> | 
| <a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br /> | 讀取/寫入<br /> | 指定用戶端控制項是否顯示提示輸入認證的對話方塊。<br /> | 
| <a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>屬性</strong></a><br /> | 讀取/寫入<br /> | 包含已命名的屬性。<br /> | 
| <a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br /> | 讀取/寫入<br /> | 指定發行者的憑證鏈。 鏈會儲存在類型 VT_BYREF 的變數中，其中包含 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> 結構的指標。<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | 讀取/寫入<br /> | 指定是否可重新導向會話中所列舉的動態連接 PnP 裝置。<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | 讀取/寫入<br /> | 指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。<br /> | 
| <a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br /> | 讀取/寫入<br /> | 控制重新導向對話方塊的存在和外觀。<br /> | 
| <a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a><br /> | 唯讀<br /> | 指定遠端監視的數目。<br /> | 
| <a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a><br /> | 唯讀<br /> | 指定遠端監視配置是否與本機監視器版面配置相同。<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | 唯讀<br /> | 用戶端 RemoteApp 設定。<br /> | 
| <a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br /> | 唯讀<br /> | 支援 <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> 介面的物件。<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | 唯讀<br /> | <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a>介面指標。<br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | 唯讀<br /> | <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a>介面的指標，用來設定用戶端控制項的安全設定。<br /> | 
| <a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br /> | 唯讀<br /> | 支援 <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> 介面的物件。<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | 唯讀<br /> | 指出 <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> 介面是否可供使用。<br /> | 
| <a href="imstscax-server.md"><strong>伺服器</strong></a><br /> | 讀取/寫入<br /> | 目前控制項所連接的伺服器名稱。<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | 讀取/寫入<br /> | 指定在啟動會話之前，是否應該顯示重新導向安全性警告對話方塊。<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | 讀取/寫入<br /> | 指出控制項是否會在啟動時立即建立 RD 工作階段主機的伺服器連接。<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | 唯讀<br /> | 用戶端 RD 閘道設定。<br /> | 
| <a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br /> | 唯讀<br /> | 要 <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>的介面。<br /> | 
| <a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br /> | 唯讀<br /> | 支援 <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> 介面的物件。<br /> | 
| <a href="imsrdpclient9-transportsettings4.md"><strong>TransportSettings4</strong></a><br /> | 唯讀<br /> | 支援 <a href="imsrdpclienttransportsettings4.md"><strong>IMsRdpClientTransportSettings4</strong></a> 介面的物件。<br /> | 
| <a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br /> | 讀取/寫入<br /> | 指定使用者啟動連線的網站是否位於用戶端電腦的 [信任的網站] 清單中。<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | 讀取/寫入<br /> | 要作為控制項父視窗的視窗控制碼。 如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。<br /> | 
| <a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a><br /> | 讀取/寫入<br /> | 指定遠端桌面 ActiveX 控制項是否應該使用多個監視器。<br /> | 
| <a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a><br /> | 讀取/寫入<br /> | 是否要使用重新導向伺服器名稱。<br /> | 
| <a href="imstscax-username.md"><strong>使用者</strong></a><br /> | 讀取/寫入<br /> | 使用者名稱登入認證。<br /> | 
| <a href="imstscax-version.md"><strong>版本</strong></a><br /> | 唯讀<br /> | 目前控制項的版本號碼。<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | 唯讀<br /> | 指出控制項是否顯示垂直捲動條。<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | 讀取/寫入<br /> | 指定在啟動會話之前，安全性警告對話方塊是否應包含關於剪貼簿重新導向的警告。<br /> | 
| <a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a><br /> | 讀取/寫入<br /> | 不會使用此屬性。<br /> | 
| <a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br /> | 讀取/寫入<br /> | 指定在啟動會話之前，重新導向對話方塊是否顯示印表機重新導向的相關訊息。<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | 讀取/寫入<br /> | 指定在啟動會話之前，安全性警告是否應包含有關將認證傳送至遠端伺服器的警告。<br /> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面 ActiveX 控制項類別](remote-desktop-activex-control-classes.md)
</dt> </dl>

