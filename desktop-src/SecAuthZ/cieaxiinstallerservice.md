---
description: 實行 IAxiService 和 IeAxiServiceCallback 介面。
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: CIeAxiInstallerService 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943503"
---
# <a name="cieaxiinstallerservice-object"></a>CIeAxiInstallerService 物件

**CIeAxiInstallerService** 物件會實 [**IAxiService**](ieaxiservice.md)和 [**IeAxiServiceCallback**](ieaxiservicecallback.md)介面。

此物件未在公用標頭中宣告。 應用程式必須自行定義。 下列介面定義語言 (IDL) 片段描述這個物件，包括其 CLSID。

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista Business、Windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




