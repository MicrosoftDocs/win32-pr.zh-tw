---
description: 表示服務識別碼的 URI。
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991929"
---
# <a name="serviceid-element"></a>ServiceID 元素

表示服務識別碼的 URI。

## <a name="usage"></a>使用方式

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>屬性

沒有任何屬性。

## <a name="child-elements"></a>子元素

沒有任何子項目。

## <a name="parent-elements"></a>父元素



| 元素                             | 描述                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**主機**](host.md)<br/>     | 定義服務主機的 **ServiceID** 和 [**Types**](types.md) 元素。 如果未明確提供，則 WSDAPI 不會提供任何預設資料來回應中繼資料要求。<br/> <br/>                                                                                                                     |
| [**託管**](hosted.md)<br/> | 定義此服務主機所提供之服務的 **ServiceID** 和 [**Types**](types.md) 元素。 這項服務主機提供的每個服務都應該有自己的 [**託管**](hosted.md) 元素資訊，以確保服務在對中繼資料要求的回應中已正確發佈。<br/> <br/> |



## <a name="element-information"></a>項目資訊



|                                     |               |
|-------------------------------------|---------------|
| 最低支援系統<br/> | Windows Vista |
| 可以是空的                        | 是           |



 

 




