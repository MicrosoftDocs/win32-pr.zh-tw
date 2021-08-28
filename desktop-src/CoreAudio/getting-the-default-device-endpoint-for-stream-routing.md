---
description: 在 Windows 7 中，使用媒體基礎、DirectSound 和 Wave api 等核心音訊 api 的高階平臺 api，藉由處理從現有裝置切換至新的預設音訊端點來執行串流路由功能。
ms.assetid: 4f36710c-c5a8-4f31-9b77-5253475c0715
title: 取得串流路由的裝置端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb45560bc8a27e4641e5d52c8fed0bee51c877dbec4d098bb5232830359f0b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695388"
---
# <a name="getting-the-device-endpoint-for-stream-routing"></a>取得串流路由的裝置端點

在 Windows 7 中，使用媒體基礎、DirectSound 和 Wave api 等核心音訊 api 的高階平臺 api，藉由處理從現有裝置切換至新的預設音訊端點來執行串流路由功能。 使用這些 Api 的媒體應用程式 (例如，在 [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)物件上啟用 **IDirectSound** 或 **IBaseFilter** 物件的應用程式) 使用串流路由行為，而不需要修改來源。

高層級 Api 會針對透過 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)取得的裝置端點，執行串流路由。 如果應用程式串流至預設裝置，資料流程路由功能會如所定義運作。 如果任何其他機制抓取資料流程，即使它與預設裝置相同，資料流程也不會切換至新的裝置。

直接使用核心音訊 Api (WASAPI 用戶端) 的媒體應用程式，可以為任何轉譯或捕獲裝置提供自訂的串流路由執行。 WASAPI 用戶端可以複寫高階 Api 所提供的實作，方法是將其限制為在設定為預設裝置的裝置上開啟的串流。 若要取得預設裝置端點的參考，用戶端必須呼叫 [**IMMDeviceEnumerator：： GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)。 在此呼叫中，用戶端必須指定 *資料流程* 參數，以指出它是否需要轉譯預設裝置的指標或 capture 預設裝置。 用戶端也必須在 **ERole** 屬性中為端點指定適當的角色 (**eConsole** 或 **eCommunications**) 。 請勿使用 **eMultimedia**。

如果應用程式串流至任何其他裝置，應用程式可以藉由呼叫 [**IMMDeviceEnumerator：： GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice)) ，藉由指定端點識別碼 (字串來取得裝置。

識別裝置之後，WASAPI 用戶端可以藉由處理針對裝置傳送的裝置和音訊會話通知，提供串流路由的執行。 如需這些通知的詳細資訊，請參閱 [串流路由的相關通知](relevant-device-notifications-for-stream-routing.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 MMDevice API](mmdevice-api.md)
</dt> <dt>

[關於 WASAPI](wasapi.md)
</dt> <dt>

[串流路由](stream-routing.md)
</dt> </dl>

 

 



