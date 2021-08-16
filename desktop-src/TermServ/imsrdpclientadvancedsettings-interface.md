---
title: IMsRdpClientAdvancedSettings 介面
description: 管理 advanced client 設定。 衍生自 IMsTscAdvancedSettings 介面。
ms.assetid: 34aeda37-9ec8-4f0a-ba92-9cf964867d5a
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings 介面遠端桌面服務
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings
- IMsRdpClientAdvancedSettings.EncryptionEnabled
- IMsRdpClientAdvancedSettings.put_EncryptionEnabled
- IMsRdpClientAdvancedSettings.get_EncryptionEnabled
- IMsRdpClientAdvancedSettings.brushSupportLevel
- IMsRdpClientAdvancedSettings.put_brushSupportLevel
- IMsRdpClientAdvancedSettings.get_brushSupportLevel
- IMsRdpClientAdvancedSettings.KeyboardType
- IMsRdpClientAdvancedSettings.put_KeyboardType
- IMsRdpClientAdvancedSettings.get_KeyboardType
- IMsRdpClientAdvancedSettings.KeyboardSubType
- IMsRdpClientAdvancedSettings.put_KeyboardSubType
- IMsRdpClientAdvancedSettings.get_KeyboardSubType
- IMsRdpClientAdvancedSettings.KeyboardFunctionKey
- IMsRdpClientAdvancedSettings.put_KeyboardFunctionKey
- IMsRdpClientAdvancedSettings.get_KeyboardFunctionKey
- IMsRdpClientAdvancedSettings.WinCEFixedPalette
- IMsRdpClientAdvancedSettings.put_WinCEFixedPalette
- IMsRdpClientAdvancedSettings.get_WinCEFixedPalette
- IMsRdpClientAdvancedSettings.ConnectWithEndpoint
- IMsRdpClientAdvancedSettings.put_ConnectWithEndpoint
- IMsRdpClientAdvancedSettings.NotifyTSPublicKey
- IMsRdpClientAdvancedSettings.put_NotifyTSPublicKey
- IMsRdpClientAdvancedSettings.get_NotifyTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ac82aa90a0a7c6d1f7e8f8774c3a85bf13f8663f9ad81bb482acb99af3ab4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657728"
---
# <a name="imsrdpclientadvancedsettings-interface"></a>IMsRdpClientAdvancedSettings 介面

管理 advanced client 設定。 衍生自 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面。 此介面包含方法，可為遠端桌面 ActiveX 控制項取出並設定 advanced (選用) 屬性。

若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。 然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings** 傳遞給 **QueryInterface**。

## <a name="members"></a>成員

**IMsRdpClientAdvancedSettings** 介面繼承自 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)。 **IMsRdpClientAdvancedSettings** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IMsRdpClientAdvancedSettings** 介面具有這些屬性。



| 屬性                                                                                                   | 存取類型           | Description                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcceleratorPassthrough**](imsrdpclientadvancedsettings-acceleratorpassthrough.md)<br/>           | 讀取/寫入<br/> | 指定是否應將鍵盤快速鍵傳遞到伺服器。<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**BitmapCacheSize**](imsrdpclientadvancedsettings-bitmapcachesize.md)<br/>                         | 讀取/寫入<br/> | 點陣圖快取檔案的大小（以 kb 為單位），用於每圖元8位的點陣圖。 這個屬性的有效值為1到32（含）。<br/>                                                                                                                                                                                                                                                                              |
| [**BitmapPersistence**](imsrdpclientadvancedsettings-bitmappersistence.md)<br/>                     | 讀取/寫入<br/> | 指定是否應該使用持續性點陣圖快取。 持續性快取可以改善效能，但需要額外的磁碟空間。<br/>                                                                                                                                                                                                                                                                                         |
| [**BitmapVirtualCache16BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)<br/> | 讀取/寫入<br/> | 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元15和16位的高色彩設定。<br/>                                                                                                                                                                                                                                                                                            |
| [**BitmapVirtualCache24BppSize**](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)<br/> | 讀取/寫入<br/> | 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於24位每圖元的高色彩設定。<br/>                                                                                                                                                                                                                                                                                                    |
| [**BitmapVirtualCacheSize**](imsrdpclientadvancedsettings-bitmapvirtualcachesize.md)<br/>           | 讀取/寫入<br/> | 指定持續性點陣圖快取檔案的大小（以 mb 為單位），以用於每圖元8位的色彩。 這個屬性的有效值為1到32（含）。 請注意，所有虛擬快取檔案的大小上限為 128 MB。 相關屬性包含 **BitmapVirtualCache16BppSize** 和 **BitmapVirtualCache24BppSize** 屬性。<br/>                                                                        |
| **brushSupportLevel**<br/>                                                                           | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CachePersistenceActive**](imsrdpclientadvancedsettings-cachepersistenceactive.md)<br/>           | 讀取/寫入<br/> | 指定是否應該使用持續性點陣圖快取。<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| [**ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md)<br/>                     | 唯寫<br/> | 指定要連接的密碼。 如需詳細資訊，請參閱 [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) 介面。<br/>                                                                                                                                                                                                                                                                           |
| [**ConnectToServerConsole**](imsrdpclientadvancedsettings-connecttoserverconsole.md)<br/>           | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| **ConnectWithEndpoint**<br/>                                                                         | 唯寫<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**DedicatedTerminal**](imsrdpclientadvancedsettings-dedicatedterminal.md)<br/>                     | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**DisableCtrlAltDel**](imsrdpclientadvancedsettings-disablectrlaltdel.md)<br/>                     | 讀取/寫入<br/> | 指定是否應顯示 Winlogon 中的初始說明畫面。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DisplayConnectionBar**](imsrdpclientadvancedsettings-displayconnectionbar.md)<br/>               | 讀取/寫入<br/> | 指定是否使用連接列。 預設值為 **VARIANT \_ TRUE**，可啟用屬性。<br/>                                                                                                                                                                                                                                                                                                              |
| [**DoubleClickDetect**](imsrdpclientadvancedsettings-doubleclickdetect.md)<br/>                     | 讀取/寫入<br/> | 指定用戶端是否識別伺服器的按兩下。<br/>                                                                                                                                                                                                                                                                                                                                                              |
| [**EnableMouse**](imsrdpclientadvancedsettings-enablemouse.md)<br/>                                 | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**EnableWindowsKey**](imsrdpclientadvancedsettings-enablewindowskey.md)<br/>                       | 讀取/寫入<br/> | 指定是否可以在遠端會話中使用 Windows 索引鍵。<br/>                                                                                                                                                                                                                                                                                                                                                               |
| **EncryptionEnabled**<br/>                                                                           | 讀取/寫入<br/> | 不支援這個屬性。 無法停用加密。<br/>                                                                                                                                                                                                                                                                                                                                                                |
| [**GrabFocusOnConnect**](imsrdpclientadvancedsettings-grabfocusonconnect.md)<br/>                   | 讀取/寫入<br/> | 指定用戶端控制項在連接時是否應該具有焦點。<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HotKeyAltEsc**](imsrdpclientadvancedsettings-hotkeyaltesc.md)<br/>                               | 讀取/寫入<br/> | 指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + ESC 的熱鍵取代。 **VK \_INSERT** 是預設值，以 ALT + INSERT 作為產生的序列。 只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。<br/>                                                                                                          |
| [**HotKeyAltShiftTab**](imsrdpclientadvancedsettings-hotkeyaltshifttab.md)<br/>                     | 讀取/寫入<br/> | 指定要新增至 ALT 的虛擬按鍵碼，以判斷 ALT + SHIFT + TAB 的替換熱鍵。 **VK \_NEXT** 是預設值，以 ALT + PAGE DOWN 作為產生的順序。 只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。<br/>                                                                                                   |
| [**HotKeyAltSpace**](imsrdpclientadvancedsettings-hotkeyaltspace.md)<br/>                           | 讀取/寫入<br/> | 指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + 空格鍵的熱鍵取代。 **VK \_DELETE** 是預設值，以 ALT + DELETE 作為產生的順序。 只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。<br/>                                                                                                              |
| [**HotKeyAltTab**](imsrdpclientadvancedsettings-hotkeyalttab.md)<br/>                               | 讀取/寫入<br/> | 指定要新增至 ALT 的虛擬金鑰程式碼，以判斷 ALT + TAB 的替換熱鍵。 **VK \_先前** 是預設值，以 ALT + PAGE UP 作為產生的序列。 只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。<br/>                                                                                                          |
| [**HotKeyCtrlAltDel**](imsrdpclientadvancedsettings-hotkeyctrlaltdel.md)<br/>                       | 讀取/寫入<br/> | 指定要新增至 CTRL + ALT 的虛擬金鑰程式碼，以決定 CTRL + ALT + DELETE 的熱鍵取代，也稱為 (SAS) 的安全注意順序。 VK \_ END 是預設值。 請注意，即使已啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性，仍不會將 CTRL + ALT + DELETE 重新導向至遠端伺服器;CTRL + ALT + DELETE 是本機 SAS 序列。<br/>                |
| [**HotKeyCtrlEsc**](imsrdpclientadvancedsettings-hotkeyctrlesc.md)<br/>                             | 讀取/寫入<br/> | 指定要新增至 ALT 的虛擬按鍵程式碼，以決定 CTRL + ESC 的熱鍵取代。 **VK \_[首頁** ] 是預設值，以 ALT + HOME 作為產生的順序。 只有在未啟用 [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) 屬性時，這個屬性才有效。<br/>                                                                                                             |
| [**HotKeyFullScreen**](imsrdpclientadvancedsettings-hotkeyfullscreen.md)<br/>                       | 讀取/寫入<br/> | 指定要新增至 CTRL + ALT 的虛擬機器碼，以決定切換至全螢幕模式的熱鍵取代。 **VK \_[取消** ] 是預設值。<br/>                                                                                                                                                                                                                                                                 |
| [**InputEventsAtOnce**](imsrdpclientadvancedsettings-inputeventsatonce.md)<br/>                     | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**keepAliveInterval**](imsrdpclientadvancedsettings-keepaliveinterval.md)<br/>                     | 讀取/寫入<br/> | 指定用戶端將 keep-alive 訊息傳送至伺服器的間隔（以毫秒為單位）。 屬性的預設值為零，它會停用 keep-alive 訊息。 這個屬性的最小有效值是10000，代表10秒。 請注意，指定是否允許持續用戶端連接到伺服器的群組原則設定，可以覆寫此屬性設定。<br/>      |
| **KeyboardFunctionKey**<br/>                                                                         | 讀取/寫入<br/> | 僅適用于 Windows CE。<br/>                                                                                                                                                                                                                                                                                                                                                                                                    |
| **KeyboardSubType**<br/>                                                                             | 讀取/寫入<br/> | 僅適用于 Windows CE。<br/>                                                                                                                                                                                                                                                                                                                                                                                                    |
| **KeyboardType**<br/>                                                                                | 讀取/寫入<br/> | 僅適用于 Windows CE。<br/>                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**LoadBalanceInfo**](imsrdpclientadvancedsettings-loadbalanceinfo.md)<br/>                         | 讀取/寫入<br/> | 指定將放置於 RD 工作階段主機 server 通訊協定連接順序中的 x.500 連接要求封包中的負載平衡 cookie。<br/>                                                                                                                                                                                                                                                                    |
| [**maxEventCount**](imsrdpclientadvancedsettings-maxeventcount.md)<br/>                             | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**MaximizeShell**](imsrdpclientadvancedsettings-maximizeshell.md)<br/>                             | 讀取/寫入<br/> | 指定是否應將以 [**StartProgram**](imstscsecuredsettings-startprogram.md) 屬性啟動的程式最大化。<br/>                                                                                                                                                                                                                                                                                              |
| [**minInputSendInterval**](imsrdpclientadvancedsettings-mininputsendinterval.md)<br/>               | 讀取/寫入<br/> | 指定傳送滑鼠事件的最小間隔（以毫秒為單位）。<br/>                                                                                                                                                                                                                                                                                                                                         |
| [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>               | 讀取/寫入<br/> | 指定用戶端在沒有使用者輸入的情況下，應維持連線的最大時間長度（以分鐘為單位）。 如果經過指定的時間，控制項會呼叫 [**IMsTscAxEvents：： OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) 方法。<br/>                                                                                                                                                      |
| **NotifyTSPublicKey**<br/>                                                                           | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**NumBitmapCaches**](imsrdpclientadvancedsettings-numbitmapcaches.md)<br/>                         | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**orderDrawThreshold**](imsrdpclientadvancedsettings-orderdrawthreshold.md)<br/>                   | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**overallConnectionTimeout**](imsrdpclientadvancedsettings-overallconnectiontimeout.md)<br/>       | 讀取/寫入<br/> | 指定用戶端控制項等候連接完成的總時間長度（以秒為單位）。 這個屬性的最大有效值為600，代表10分鐘。 如果在連接完成之前指定的時間，控制項就會中斷連接，並呼叫 [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md) 方法。 相關的屬性為 **singleConnectionTimeout**。<br/> |
| [**PerformanceFlags**](imsrdpclientadvancedsettings-performanceflags.md)<br/>                       | 讀取/寫入<br/> | 指定可在伺服器上設定的一組功能，以改善效能。<br/>                                                                                                                                                                                                                                                                                                                                             |
| [**PersistCacheDirectory**](imsrdpclientadvancedsettings-persistcachedirectory.md)<br/>             | 唯寫<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**PinConnectionBar**](imsrdpclientadvancedsettings-pinconnectionbar.md)<br/>                       | 讀取/寫入<br/> | 指定 UI 連接列的狀態。 將此屬性設定為 **VARIANT \_ TRUE** 會將狀態設定為「減少」，也就是使用者看不到，而且無法輸入。 **變異 \_FALSE** 會將狀態設定為「已引發」，並可供使用者輸入。<br/>                                                                                                                                                                   |
| [**RdpdrClipCleanTempDirString**](imsrdpclientadvancedsettings-rdpdrclipcleantempdirstring.md)<br/> | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**RdpdrClipPasteInfoString**](imsrdpclientadvancedsettings-rdpdrclippasteinfostring.md)<br/>       | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**RdpdrLocalPrintingDocName**](imsrdpclientadvancedsettings-rdpdrlocalprintingdocname.md)<br/>     | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**RDPPort**](imsrdpclientadvancedsettings-rdpport.md)<br/>                                         | 讀取/寫入<br/> | 指定連接通訊埠。 預設值為3389。<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**RedirectDrives**](imsrdpclientadvancedsettings-redirectdrives.md)<br/>                           | 讀取/寫入<br/> | 指定是否允許重新導向磁片磁碟機。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**RedirectPorts**](imsrdpclientadvancedsettings-redirectports.md)<br/>                             | 讀取/寫入<br/> | 指定是否允許重新導向本機埠 (例如，COM 和 LPT) 。<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**RedirectPrinters**](imsrdpclientadvancedsettings-redirectprinters.md)<br/>                       | 讀取/寫入<br/> | 指定是否允許印表機的重新導向。<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| [**RedirectSmartCards**](imsrdpclientadvancedsettings-redirectsmartcards.md)<br/>                   | 讀取/寫入<br/> | 指定是否允許智慧卡的重新導向。<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**SasSequence**](imsrdpclientadvancedsettings-sassequence.md)<br/>                                 | 讀取/寫入<br/> | 指定用戶端將用來存取伺服器上登入畫面的安全存取順序。<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ScaleBitmapCachesByBPP**](imsrdpclientadvancedsettings-scalebitmapcachesbybpp.md)<br/>           | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**ShadowBitmap**](imsrdpclientadvancedsettings-shadowbitmap.md)<br/>                               | 讀取/寫入<br/> | 不支援這個屬性。<br/> **Windows Vista：** 指定是否應該使用陰影點陣圖。<br/>                                                                                                                                                                                                                                                                                                                     |
| [**shutdownTimeout**](imsrdpclientadvancedsettings-shutdowntimeout.md)<br/>                         | 讀取/寫入<br/> | 指定等待伺服器回應中斷連接要求的時間長度（以秒為單位）。 屬性的預設值為10。 屬性的最大有效值為600，代表10分鐘。 如果伺服器未在指定的時間內回復，用戶端控制項就會中斷連線。<br/>                                                                                                         |
| [**singleConnectionTimeout**](imsrdpclientadvancedsettings-singleconnectiontimeout.md)<br/>         | 讀取/寫入<br/> | 指定用戶端控制項等候 IP 位址連線的最大時間長度（以秒為單位）。 在連接期間，控制項可能會嘗試連接至多個 IP 位址。 這個屬性的最大有效值為600。 相關的屬性為 **overallConnectionTimeout**。<br/>                                                                                                                        |
| [**SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md)<br/>                                 | 讀取/寫入<br/> | 指定是否應調整顯示器大小以符合控制項的工作區。 **變異 \_TRUE** 可進行調整。 請注意，當 **SmartSizing** 屬性已啟用時，不會顯示捲軸。<br/>                                                                                                                                                                                                                         |
| [**SmoothScroll**](imsrdpclientadvancedsettings-smoothscroll.md)<br/>                               | 讀取/寫入<br/> | 不支援這個屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**TransportType**](imsrdpclientadvancedsettings-transporttype.md)<br/>                             | 讀取/寫入<br/> | 指定用戶端所使用的傳輸類型。 遠端桌面 ActiveX 控制項不會使用這個屬性。<br/>                                                                                                                                                                                                                                                                                                             |
| **WinCEFixedPalette**<br/>                                                                           | 讀取/寫入<br/> | 僅適用于 Windows CE。<br/>                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：

-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

當控制項已連接時，除非另有指示，否則無法設定這個屬性。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                        |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                  |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面網頁連線參考](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

