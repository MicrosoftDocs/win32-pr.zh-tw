---
title: IWMDRMProvider 介面
description: IWMDRMProvider 介面所提供的方法會建立 Microsoft Windows Media DRM 用戶端擴充 Api 的其他物件。您可以藉由呼叫 WMDRMCreateProvider 函式，取得這個介面實例的指標。
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- IWMDRMProvider 介面 windows 媒體格式
- IWMDRMProvider 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682836"
---
# <a name="iwmdrmprovider-interface"></a>IWMDRMProvider 介面

**IWMDRMProvider** 介面提供的方法會建立 Microsoft WINDOWS Media DRM 用戶端擴充 api 的其他物件。

您可以藉由呼叫 [**WMDRMCreateProvider**](wmdrmcreateprovider.md) 函式來取得這個介面實例的指標。 若要取得可建立安全物件之這個介面實例的指標，您必須呼叫 [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) 函數。

## <a name="members"></a>成員

**IWMDRMProvider** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMProvider** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMProvider** 介面具有這些方法。



| 方法                                              | 描述                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**CreateObject**](iwmdrmprovider-createobject.md) | 抓取指定介面的指標，視需要建立執行物件。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> </dl>

 

