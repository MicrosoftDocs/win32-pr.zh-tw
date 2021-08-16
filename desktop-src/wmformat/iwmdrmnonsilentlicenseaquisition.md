---
title: IWMDRMNonSilentLicenseAquisition 介面
description: IWMDRMNonSilentLicenseAquisition 介面提供的方法可啟用授權取得，而需要使用者介入。您可以藉由執行非無訊息授權取得來取得這個介面。
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- IWMDRMNonSilentLicenseAquisition 介面 windows 媒體格式
- IWMDRMNonSilentLicenseAquisition 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c953588cb457e8afb21cca38e9daed08b2387ab9fb7871ecd6b17dae9dca152f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110348"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>IWMDRMNonSilentLicenseAquisition 介面

**IWMDRMNonSilentLicenseAquisition** 介面提供的方法可啟用授權取得，而需要使用者介入。

您可以藉由執行非無訊息授權取得來取得這個介面。 在您呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 之後，將會產生 **MEWMDRMLicenseAcquisitionCompleted** 事件。 呼叫事件的 **IMFMediaEvent：： GetValue** 方法，取得可查詢此介面之實例指標的 **IUnknown** 介面指標。

## <a name="members"></a>成員

**IWMDRMNonSilentLicenseAquisition** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMNonSilentLicenseAquisition** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMNonSilentLicenseAquisition** 介面具有這些方法。



| 方法                                                                | 描述                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | 抓取應張貼至授權伺服器的授權挑戰。<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | 抓取授權挑戰應張貼至其中的 URL。<br/>           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> <dt>

[**取得非無訊息授權**](non-silent-license-acquisition.md)
</dt> </dl>

 

