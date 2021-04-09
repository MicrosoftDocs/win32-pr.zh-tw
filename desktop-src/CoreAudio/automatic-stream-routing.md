---
description: 本文說明如何更新 WASAPI 的執行，以利用自動串流路由。
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: 自動串流路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936495"
---
# <a name="automatic-stream-routing"></a>自動串流路由

本文說明如何更新 WASAPI 的執行，以利用自動串流路由。

從 Windows 7 開始，每當預設音訊裝置變更時，就會將應用程式的音訊播放串流順暢地從先前的預設音訊裝置傳輸到新的預設音訊裝置。 此傳輸會自動發生，不需要任何額外的應用程式程式碼。 不過，在 Windows 10 之前的1607版中，使用低層級 Windows 音訊會話 API (WASAPI) 的應用程式無法參與此自動化串流路由功能。 使用 WASAPI 的應用程式必須藉由新增額外的程式碼來偵測音訊裝置的抵達和移除，並適當地將串流切換至這些裝置，以執行自己的串流路由形式。 使用 WASAPI 的應用程式不會在裝置抵達或移除 risked 上執行自己的串流路由機制，以提供不理想的使用者體驗。

從 Windows 10 版本1607開始，使用 WASAPI 的應用程式可以利用自動串流路由。 如果您的應用程式使用 WASAPI，強烈建議您使用下列步驟來更新應用程式，以利用這項新功能：

1.  Windows 10 1607 版中，定義了兩個新的 Guid，可用來啟用具有自動串流路由的音訊轉譯或捕捉介面 [， \_ DEVINTERFACE \_ 音訊](/windows/desktop/CoreAudio/devinterface-xxx-guids) 轉譯和 [DEVINTERFACE \_ 音訊 \_ 捕獲](/windows/desktop/CoreAudio/devinterface-xxx-guids)。 藉由呼叫 [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid)來取得這些 guid 的字串表示。 下列範例顯示音訊轉譯 GUID 的這個呼叫。

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  將識別碼字串傳遞至 WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) 函式，以啟用音訊端點。 下列範例會傳遞在步驟1中取得的音訊轉譯識別碼：

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  釋放配置用來保存端點識別碼的記憶體：

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

在您修改應用程式以上述方式啟動音訊介面之後，它會參與自動串流路由功能。

若要示範自動串流路由，請使用配備內部喇叭的膝上型電腦或平板電腦播放音訊。 您應該會聽到透過裝置的內部喇叭播放音訊。 播放音訊時，連接一組耳機。 您現在應該會聽到透過耳機播放音訊。 然後，拔掉耳機和音訊應該會自動路由回內部喇叭。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流路由](stream-routing.md)
</dt> <dt>

[**MediaDevice.GetDefaultAudioRenderId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[**MediaDevice.GetDefaultAudioCaptureId**](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
