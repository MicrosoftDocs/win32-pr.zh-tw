---
description: 本節包含將已淘汰的行動寬頻 Win32 api 移植至相等 Windows 執行階段 api 的參考資料。
title: 將 Mobile 寬頻 Win32 api 移植至 Windows 執行階段 api 的指導方針
ms.topic: reference
ms.date: 08/23/2021
ms.openlocfilehash: 4cbe0415e40f18d372fdd8b9089dbd4afe197b38
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767705"
---
# <a name="guidelines-for-porting-mobile-broadband-win32-apis-to-windows-runtime-apis"></a>將 Mobile 寬頻 Win32 api 移植至 Windows 執行階段 api 的指導方針

下表列出已淘汰之行動寬頻 Win32 api 的對等 Windows 執行階段功能。

| **IMbnConnection** |  相等的 Windows 執行階段功能 |
| - | - |
| 連線 | ConnectivityManager.AcquireConnectionAsync |
| 中斷連線 | ConnectionSession。關閉 |
| 取得 \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetActivationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| GetConnectionState | WwanConnectionProfileDetails.GetNetworkRegistrationState |
| GetVoiceCallState | MobileBroadbandNetwork.GetVoiceCallSupport, PhoneCallManager.IsCallActive |
| **IMbnConnectionEvents** | |
| OnConnectComplete | NetworkStateChangeEventDetails. HasNewWwanRegistrationState –在通知之後，可以從 WwanConnectionProfileDetails. GetNetworkRegistrationState 中取出目前的註冊狀態。 |
| OnConnectStateChange | NetworkStateChangeEventDetails. HasNewWwanRegistrationState –在通知之後，可以從 WwanConnectionProfileDetails. GetNetworkRegistrationState 中取出目前的註冊狀態。 |
| OnDisconnectComplete | NetworkStateChangeEventDetails. HasNewWwanRegistrationState –在通知之後，可以從 WwanConnectionProfileDetails. GetNetworkRegistrationState 中取出目前的註冊狀態。 |
| OnVoiceCallStateChange | PhoneCallManager.CallStateChanged |
| **IMbnConnectionProfile** | |
| 刪除 | ConnectionProfile.TryDeleteAsync |
| GetConnectionProfile | NetworkAdapter. GetConnectedProfileAsync |
| GetConnectionProfiles | System.net.networkinformation.networkinformationexception. GetConnectionProfiles |
| **IMbnDeviceService** | |
| CloseCommandSession | MobileBroadbandDeviceServiceCommandSession.CloseSession |
| CloseDataSession | MobileBroadbandDeviceServiceDataSession.CloseSession |
| 取得 \_ DeviceServiceID | MobileBroadbandDeviceService.DeviceServiceId |
| OpenCommandSession | MobileBroadbandDeviceService.OpenCommandSession |
| OpenDataSession | MobileBroadbandDeviceService.OpenDataSession |
| QueryCommand | MobileBroadbandDeviceServiceCommandSession.SendQueryCommandAsync |
| QuerySupportedCommands | MobileBroadbandDeviceService.SupportedCommands |
| SetCommand | MobileBroadbandDeviceServiceCommandSession.SendSetCommandAsync |
| WriteData | MobileBroadbandDeviceServiceDataSession.WriteDataAsync |
| **IMbnDeviceServicesCoNtext** | |
| EnumerateDeviceServices | MobileBroadbandDeviceService.SupportedCommands |
| 取得 \_ MaxCommandSize | MobileBroadbandModem.MaxDeviceServiceCommandSizeInBytes |
| 取得 \_ MaxDataSize | MobileBroadbandModem.MaxDeviceServiceDataSizeInByte |
| GetDeviceService | MobileBroadbandModem.GetDeviceService |
| **IMbnDeviceServicesEvents** | |
| OnReadData | MobileBroadbandDeviceServiceDataSession. DataReceived |
| **IMbnInterface** | |
| 取得 \_ InterfaceID | MobileBroadbandAccount.NetworkAccountId |
| GetConnection | 從 AcquireConnectionAsync 取得的 ConnectionSession |
| GetHomeProvider | MobileBroadbandModem.GetCurrentConfigurationAsync |
| GetInterfaceCapability | MobileBroadbandAccount.CurrentDeviceInformation |
| GetReadyState | MobileBroadbandDeviceInformation.NetworkDeviceStatus |
| GetSubscriberInformation | MobileBroadbandAccount.CurrentDeviceInformation |
| InEmergencyMode | MobileBroadbandModem.IsInEmergencyCallMode |
| **IMbnInterfaceEvents** | |
| OnEmergencyModeChange | MobileBroadbandModem.IsInEmergencyCallModeChanged |
| OnReadyStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnSubscriberInformationChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnInterfaceManager** | |
| GetInterface | MobileBroadbandModem.CurrentAccount |
| **IMbnInterfaceManagerEvents** | |
| OnInterfaceArrival | MobileBroadbandAccountWatcher.AccountAdded |
| OnInterfaceRemoval | MobileBroadbandAccountWatcher 帳戶 |
| **IMbnMultiCarrier** | |
| GetCurrentCellularClass | MobileBroadbandDeviceInformation.CellularClass |
| **IMbnMultiCarrierEvents** | |
| OnCurrentCellularClassChange | MobileBroadbandAccountUpdatedEventArgs.HasDeviceInformationChanged |
| **IMbnPin** | |
| 變更 | MobileBroadbandPin.ChangeAsync |
| 停用 | MobileBroadbandPin.DisableAsync |
| 啟用 | MobileBroadbandPin.EnableAsync |
| Enter | MobileBroadbandPin.EnterAsync |
| 取得 \_ PinFormat | MobileBroadbandPin。格式 |
| 取得 \_ PinLengthMax | MobileBroadbandPin MaxLength |
| 取得 \_ PinLengthMin | MobileBroadbandPin MaxLength |
| 取得 \_ PinMode | MobileBroadbandPin。已啟用 |
| 取得 \_ PinType | MobileBroadbandPin。類型 |
| GetPinManager | MobileBroadbandDeviceInformation.PinManager |
| 疏通 | MobileBroadbandPin.UnblockAsync |
| **IMbnPinManager** | |
| GetPin | MobileBroadbandPinManager.GetPin |
| GetPinList | MobileBroadbandPinManager.SupportedPins |
| GetPinState | MobileBroadbandPin.LockState |
| **IMbnPinManagerEvents** | |
| **IMbnRadio** | |
| 取得 \_ SoftwareRadioState | GetRadiosAsync –無線電波。 狀態 |
| SetSoftwareRadioState | SetStateAsync |
| **IMbnRadioEvents** | |
| OnRadioStateChange | StateChanged |
| **IMbnRegistration** | |
| GetAvailableDataClasses | MobileBroadbandDeviceInformation. Dataclasses.dll |
| GetCurrentDataClass | MobileBroadbandNetwork.RegisteredDataClass |
| GetPacketAttachNetworkError | MobileBroadbandNetwork.PacketAttachNetworkError |
| GetProviderID | MobileBroadbandNetwork.RegisteredProviderId |
| GetProviderName | MobileBroadbandNetwork.RegisteredProviderName |
| GetRegisterState | MobileBroadbandNetwork.NetworkRegistrationState |
| GetRegistrationNetworkError | MobileBroadbandNetwork.ActivationNetworkError |
| **IMbnRegistrationEvents** | |
| OnPacketServiceStateChange | MobileBroadbandNetworkRegistrationStateChange |
| OnRegisterStateChange | MobileBroadbandNetworkRegistrationStateChange |
| GetSignalStrength | ConnectionProfile. GetSignalBar/MobileBroadbandCellLte. ReferenceSignalReceivedPowerInDBm/MobileBroadbandCellGsm. ReceivedSignalStrengthInDBm |
| **IMbnSignalEvents** | |
| **IMbnSms** | |
| GetSmsConfiguration | SmsDevice2. SmscAddress、SmsDevice2 CellularClass、CDMAShortMessageSize 和 MaxMessageIndex 不需要作為公用 API。 |
| SetSmsConfiguration | SmsDevice2. SmscAddress，不支援任何其他參數 |
| SmsSendCdma | 在 ISmsMessageBase 中使用 CellularClass 的 SendMessageAndGetResultAsync |
| SmsSendCdmaPdu | 在 ISmsMessageBase 中使用 Messagetype 和 CellularClass 的 SendMessageAndGetResultAsync |
| SmsSendPdu | 在 ISmsMessageBase 中使用 MessageType 的 SendMessageAndGetResultAsync |
| **IMbnSmsConfiguration** | |
| 取得 \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| 取得 \_ SmsFormat | SmsDevice2.CellularClass |
| put \_ ServiceCenterAddress | SmsDevice2.SmscAddress |
| **IMbnSmsEvents** | |
| OnSmsNewClass0Message | SmsMessageRegistration. MessageReceived |
| OnSmsSendComplete | SmsSendMessageResult |
| **IMbnSmsReadMsgPdu** | |
| 取得 \_ 訊息 | SmsTextMessage2 |
| 取得 \_ PduData | SmsTextmessage2 |
| **IMbnSmsReadMsgTextCdma** | |
| 取得 \_ 位址 | SmsTextMessage2 |
| 取得 \_ EncodingID | SmsTextMessage2 編碼 |
| 取得 \_ 訊息 | SmsTextMessage2 |
| 取得 \_ 時間戳記 | SmsTextMessage.2Timestamp |
| **IMbnSubscriberInformation** | |
| 取得 \_ SimIccID | MobileBroadbandDeviceInformation.SimIccId |
| 取得 \_ SubscriberID | MobileBroadbandDeviceInformation.SubscriberId |
| 取得 \_ TelephoneNumbers | MobileBroadbandDeviceInformation.TelephoneNumbers |
