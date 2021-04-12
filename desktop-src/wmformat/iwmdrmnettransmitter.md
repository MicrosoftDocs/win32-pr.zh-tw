---
title: IWMDRMNetTransmitter 介面
description: IWMDRMNetTransmitter 介面提供了使用網路裝置的 Windows Media DRM 作為傳輸器所需的方法。若要取得這個介面的實例，請呼叫 IWMDRMProvider CreateObject。 將 IID \_ IWMDRMNetTransmitter 傳遞為 riid 參數。
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- IWMDRMNetTransmitter 介面 windows 媒體格式
- IWMDRMNetTransmitter 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315754"
---
# <a name="iwmdrmnettransmitter-interface"></a>IWMDRMNetTransmitter 介面

**IWMDRMNetTransmitter** 介面提供了使用網路裝置的 WINDOWS Media DRM 作為傳輸器所需的方法。

若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。 將 **IID \_ IWMDRMNetTransmitter** 傳遞為 *riid* 參數。

## <a name="members"></a>成員

**IWMDRMNetTransmitter** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMNetTransmitter** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMNetTransmitter** 介面具有這些方法。



| 方法                                                                        | 描述                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | 產生分葉授權回應訊息。<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | 產生根授權回應訊息<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | 處理 Microsoft Windows Media DRM 為網路裝置接收器傳送的授權挑戰<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMNetReceiver 介面**](iwmdrmnetreceiver.md)
</dt> </dl>

 

