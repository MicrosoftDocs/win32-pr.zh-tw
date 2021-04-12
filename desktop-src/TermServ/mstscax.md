---
title: MsTscAx 類別
description: Microsoft 終端機服務用戶端控制 (可轉散發套件) -第1版。
ms.assetid: 8B8FEF40-89A5-47C0-94EE-4F4B2B5738AB
ms.tgt_platform: multiple
keywords:
- MsTscAx 類別遠端桌面服務
- MsTscAx 類別遠端桌面服務，說明
topic_type:
- apiref
api_name:
- MsTscAx
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62ed4bdaf25bfaf7603becbb13444d3a3b23cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384281"
---
# <a name="mstscax-class"></a>MsTscAx 類別

Microsoft 終端機服務用戶端控制 (可轉散發套件) -第1版

這個類別會執行下列介面。

-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)

**MsTscAx** 具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MsTscAx** 類別有這些方法。



| 方法                                                                                      | 描述                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**連接**](imstscax-connect.md)                                                         | 使用目前在控制項上設定的屬性起始連接。<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | 針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。<br/>                                                                                                                                                                                              |
| [**中斷連線**](imstscax-disconnect.md)                                                   | 中斷使用中連接。<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | 抓取為虛擬通道設定的選項。<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | 通知遠端桌面 ActiveX 控制項的裝置重新導向模組，表示系統上已發生裝置變更。 這個方法會將 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 通知傳遞給控制項。<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | 在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | 在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | 當用戶端控制項自動重新連接到遠端會話時呼叫。<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | 當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | 當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | 當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | 當用戶端呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時呼叫。<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | 當用戶端控制項正在建立與 RD 工作階段主機 server 的連接時呼叫。<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | 當用戶端控制項開始連接到伺服器以回應 [**IMsTscAx：： Connect**](imstscax-connect.md)的呼叫時呼叫。<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | 當使用者在連接列上向下拖曳時呼叫。<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | 當按下連接列中的 [裝置] 按鈕時呼叫。<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | 當用戶端控制項與 RD 工作階段主機伺服器中斷連線時呼叫。<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | 當用戶端進入全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | 當用戶端控制項遇到嚴重錯誤時呼叫。<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | 在按下放開焦點按鍵組合時呼叫。 例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | 當使用者在 [**IMsRdpClientAdvancedSettings：:p 長 \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 方法設定期間沒有滑鼠或鍵盤輸入時呼叫。<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | 當用戶端離開全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | 當用戶端控制項成功登入 RD 工作階段主機伺服器時呼叫，並遵循 Windows 登入對話方塊的顯示。<br/>                                                                                                                                      |
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
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | 要求正常關機用戶端控制項。<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | 重設控制項中的所有密碼狀態。<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | 將一連串的按鍵傳送到控制項。 按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | 透過先前使用 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至 RD 工作階段主機伺服器。<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | 設定用戶端控制項的虛擬通道選項。<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>屬性

**MsTscAx** 類別具有這些屬性。



| 屬性                                                                             | 存取類型           | Description                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | 唯讀<br/>  | [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)介面指標。<br/>                                                                       |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | 唯讀<br/>  | [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)介面的指標，用來設定用戶端控制項的 advanced 設定。<br/> |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>              | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                      | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | 唯讀<br/>  | 目前控制項的最大加密強度。<br/>                                                                                                        |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>        | 唯寫<br/> | 以純文字格式的遠端桌面 ActiveX 控制項密碼。<br/>                                                                                              |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | 讀取/寫入<br/> | 目前控制項的色彩深度。<br/>                                                                                                                            |
| [**連線**](imstscax-connected.md)<br/>                                   | 唯讀<br/>  | 目前控制項的連接狀態。<br/>                                                                                                                   |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | 讀取/寫入<br/> | 控制項連接時，顯示在控制項中央的文字。<br/>                                                                                 |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | 讀取/寫入<br/> | 目前的控制項在初始遠端桌面上的高度（以圖元為單位）。<br/>                                                                                        |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | 讀取/寫入<br/> | 目前的控制項寬度（以圖元為單位），在初始的遠端桌面。<br/>                                                                                         |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | 讀取/寫入<br/> | 在連接結束之前出現在控制項中央的文字。<br/>                                                                               |
| [**域**](imstscax-domain.md)<br/>                                         | 讀取/寫入<br/> | 目前使用者登入的網域。<br/>                                                                                                                  |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | 唯讀<br/>  | 有關用戶端控制項中斷連接原因的詳細資訊。<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | 讀取/寫入<br/> | 指出控制項是否處於全螢幕模式。<br/>                                                                                                          |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | 唯寫<br/> | 當控制項處於全螢幕模式時，所顯示的視窗標題。<br/>                                                                                            |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | 唯讀<br/>  | 指出控制項是否已顯示水準捲軸。<br/>                                                                                           |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>          | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                  | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | 唯讀<br/>  | [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)介面指標。<br/>                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | 唯讀<br/>  | [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)介面的指標，用來設定用戶端控制項的安全設定。<br/>    |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | 唯讀<br/>  | 指出 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) 介面是否可供使用。<br/>                                                 |
| [**伺服器**](imstscax-server.md)<br/>                                         | 讀取/寫入<br/> | 目前控制項所連接的伺服器名稱。<br/>                                                                                              |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | 讀取/寫入<br/> | 指出控制項是否會在啟動時立即建立 RD 工作階段主機的伺服器連接。<br/>                                                   |
| [**使用者**](imstscax-username.md)<br/>                                     | 讀取/寫入<br/> | 使用者名稱登入認證。<br/>                                                                                                                                |
| [**版本**](imstscax-version.md)<br/>                                       | 唯讀<br/>  | 目前控制項的版本號碼。<br/>                                                                                                                     |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | 唯讀<br/>  | 指出控制項是否顯示垂直捲動條。<br/>                                                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsTscAx 定義為 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面 ActiveX 控制項類別](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

