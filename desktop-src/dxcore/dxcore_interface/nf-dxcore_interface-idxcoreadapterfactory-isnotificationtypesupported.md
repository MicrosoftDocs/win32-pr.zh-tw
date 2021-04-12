---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: 判斷作業系統 (OS) 是否支援指定的通知類型。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315967"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>IDXCoreAdapterFactory：： IsNotificationTypeSupported 方法

判斷作業系統 (OS) 是否支援指定的通知類型。 如需程式設計指引和程式碼範例，請參閱 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)。

## <a name="syntax"></a>語法

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>參數

### <a name="notificationtype"></a>notificationType

類型： **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

您要查詢有關支援的通知類型。 如需通知類型的相關資訊，請參閱 [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) 中的表格。

## <a name="returns"></a>傳回

類型： **bool**

 `true`   如果系統支援通知型別，則會傳回。 否則，會傳回  `false` 。

## <a name="remarks"></a>備註

您可以呼叫 **IsNotificationTypeSupported** ，判斷這個作業系統版本是否知道指定的通知類型。 例如，在特定版本的 Windows 中引進的通知類型，對於舊版 Windows 而言是未知的。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md)、 [DXCore 參考](../dxcore-reference.md)、 [DXCore 介面卡屬性 guid](../dxcore-adapter-attribute-guids.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)