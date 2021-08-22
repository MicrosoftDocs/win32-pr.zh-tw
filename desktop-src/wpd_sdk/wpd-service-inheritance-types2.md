---
description: 指定服務的繼承關聯性。
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: 'WPD_SERVICE_INHERITANCE_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5a0e69986e7415a5a12eca7c450b0d7ff064c650d33c35997b9a166b01592c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444798"
---
# <a name="wpd_service_inheritance_types-enumeration"></a>WPD \_ 服務 \_ 繼承 \_ 類型列舉

**WPD \_ 服務 \_ 繼承 \_ 類型** 列舉型別會指定服務的繼承關聯性。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**WPD \_ 服務 \_ 繼承的 \_ 執行**
</dt> <dd>

服務會藉由執行抽象服務定義來繼承。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceServiceCapabilities::GetInheritedServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




