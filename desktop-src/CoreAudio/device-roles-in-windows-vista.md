---
description: 使用裝置角色
ms.assetid: 3b2cb1fe-0f11-4509-a6f3-513d2755cd29
title: 使用裝置角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21ea667a6974634c1f9f0657dd02c13a621641c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936051"
---
# <a name="working-with-device-roles"></a>使用裝置角色

[MMDEVICE API](mmdevice-api.md)支援裝置角色。 [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)列舉會定義 MMDevice API 所支援的裝置角色。

> [!Note]  
> 雖然 [MMDEVICE API](mmdevice-api.md) 支援裝置角色，但 Windows Vista 中的使用者介面並不支援此功能。

 

應用程式可以透過 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)和 [**IMMNotificationClient：： OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)方法，使用 MMDevice API 來支援 [裝置角色](device-roles.md)。 不過，Windows Vista 中的使用者介面不支援將個別角色指派給不同的裝置。 在 Windows Vista 中，使用者介面可讓使用者選取用於轉譯的預設音訊裝置，以及用於捕捉的預設音訊裝置。 當使用者選取預設轉譯或捕獲裝置時，系統會將這三個裝置角色 (eConsole、eMultimedia 和 eCommunications) 指派給該裝置。 應用程式無法變更指派給音訊端點裝置的角色。 作業系統只允許使用者指派裝置角色。

用戶端可以註冊自己，以在每次將角色指派給音訊端點裝置時，收到來自 MMDevice API 的通知。 當角色從某個裝置移到另一個裝置時，用戶端可以選擇是否要繼續播放 (或透過相同裝置錄製) 的串流，或將串流切換到其他裝置。 根據預設，資料流程會繼續播放 (或透過原始裝置記錄) 。 在 Windows Vista 中，若要將串流切換至另一個裝置，用戶端必須刪除原始裝置上的資料流程，並在新裝置上建立替代串流。 在 Windows 7 中，用戶端可以接聽新的通知，以在不中斷播放或捕捉會話的情況下，執行無縫切換。 如需詳細資訊，請參閱 [資料流程路由](stream-routing.md)。

如果您打算使用 Windows Vista 來測試您的應用程式，您可以設定測試環境，以確認當使用者可以將個別裝置角色指派給不同的裝置時，應用程式會如預期般運作。 如需詳細資訊，請傳送電子郵件至：uaa@microsoft.com。

## <a name="communication-devices"></a>通訊裝置

Windows 7 使用者介面具有新增 *通訊裝置* 的功能。 **音效** 控制台可讓使用者選取預設通訊裝置，以轉譯和捕獲音訊串流。 根據預設，當新的裝置連接到電腦時，作業系統會執行自動角色偵測，並判斷裝置是否適合 eCommunication 角色。 藉由將通訊裝置設為目標，您可以開發使用核心音訊 Api 的應用程式來實行電腦電話通訊解決方案。 例如，VoIP 應用程式可能會將其語音輸入和輸出串流指派給預設的捕獲，並以 eCommunications 角色呈現端點裝置。 與任何其他串流一樣，通訊應用程式必須藉由呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)來取得通訊裝置端點的參考。 在此呼叫中，應用程式必須在 *Role* 參數中指定 **eCommunications** 。 在通訊裝置上開啟之資料流程上的 WASAPI 資料流程作業，類似于任何其他音訊串流。 通訊應用程式可以藉由處理來自裝置端點的通知，來強化使用者體驗，例如回避。 如需詳細資訊，請參閱 [使用通訊裝置](using-the-communication-device.md)。

## <a name="automatic-device-role-detection"></a>自動裝置角色偵測

假設電腦具有預設轉譯裝置、喇叭和預設捕獲裝置（麥克風）的情況。 使用者將 USB 耳機連接到電腦。 安裝適當的驅動程式之後，作業系統會嘗試偵測要為新的音訊裝置指派的角色。

在 Windows 7 中，已大幅改善裝置角色偵測功能，以判斷適合音訊裝置的適當角色。 所有音訊裝置都包含一組由裝置 OEM 填入的設定設定，可協助系統決定如何使用該裝置。 這些設定包括音訊插座的實體位置、裝置類型、插座子類型，以及偵測功能等資訊，讓系統可以判斷裝置是否已插入。 藉由從裝置中取出這些值，作業系統會決定要指派給裝置的角色。 在此案例中，系統已查詢 USB 耳機裝置、執行自動角色偵測，並決定裝置最適合作為通訊裝置。

應用程式也可以使用核心音訊 Api 來取得插座資訊。 如需詳細資訊，請參閱 [**IKsJackDescription**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription) 和 [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[裝置角色](device-roles.md)
</dt> </dl>

 

 



