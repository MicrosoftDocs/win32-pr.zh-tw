---
title: IWMDRMIndividualizationStatus 介面
description: IWMDRMIndividualizationStatus 介面可讓您抓取有關個人化進度的 advanced status 資訊。此介面會與 MEWMDRMIndividualizationProgress 事件一起傳遞。
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- IWMDRMIndividualizationStatus 介面 windows 媒體格式
- IWMDRMIndividualizationStatus 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6242d2c66b165be8c750d71c61020e9a6acc66f68654d73898fd5000ace3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701467"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>IWMDRMIndividualizationStatus 介面

**IWMDRMIndividualizationStatus** 介面可讓您抓取有關個人化進度的 advanced status 資訊。

此介面會與 MEWMDRMIndividualizationProgress 事件一起傳遞。 在 IWMDRMSecurity 的呼叫之間會產生許多這類事件 [**：:P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) 和自動完成的個人化程式（由產生 **MEWMDRMIndividualizationCompleted** 事件發出信號）。

若要取出 **IWMDRMIndividualizationStatus** 介面實例的指標，您必須先呼叫進度事件的 **IMFMediaEvent：： GetValue** 方法。 您從事件中取出的值是實 **IWMDRMIndividualizationStatus** 介面之物件的 **IUnknown** 介面指標。

## <a name="members"></a>成員

**IWMDRMIndividualizationStatus** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMIndividualizationStatus** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMIndividualizationStatus** 介面具有這些方法。



| 方法                                                       | 描述                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | 抓取有關個人化的詳細資訊。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> </dl>

 

