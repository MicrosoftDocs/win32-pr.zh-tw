---
title: IWMDRMNetReceiver 介面
description: IWMDRMNetReceiver 介面提供使用 Microsoft Windows Media DRM 做為接收器的網路裝置所需的方法。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMNetReceiver 傳遞為 riid 參數。
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- IWMDRMNetReceiver 介面 windows 媒體格式
- IWMDRMNetReceiver 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373397"
---
# <a name="iwmdrmnetreceiver-interface"></a>IWMDRMNetReceiver 介面

**IWMDRMNetReceiver** 介面提供使用 Microsoft WINDOWS Media DRM 做為接收器的網路裝置所需的方法。

若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。 將 **IID \_ IWMDRMNetReceiver** 傳遞為 *riid* 參數。

## <a name="members"></a>成員

**IWMDRMNetReceiver** 介面繼承自 [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)。 **IWMDRMNetReceiver** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMNetReceiver** 介面具有這些方法。



| 方法                                                                               | 描述                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | 產生當要求受保護的內容時，傳送給發送器的授權挑戰。<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | 產生註冊挑戰，在接收者註冊或重新驗證時傳送給發送器。<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | 處理傳輸器在回復至授權挑戰時傳送的授權回應。<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | 處理傳輸器在回復註冊挑戰時傳送的註冊回應。<br/>                    |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**IWMDRMNetTransmitter 介面**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





