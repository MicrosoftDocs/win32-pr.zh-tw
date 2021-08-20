---
title: IMsRdpClient10 RemoteProgram3 屬性
description: 支援 ITSRemoteProgram3 介面的物件。
ms.assetid: afb26152-32eb-45de-a228-a6f7ca7eea2b
ms.tgt_platform: multiple
keywords:
- RemoteProgram3 屬性遠端桌面服務
- RemoteProgram3 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，RemoteProgram3 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient10.RemoteProgram3
- IMsRdpClient10.get_RemoteProgram3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f332985777d6b83e04724e6bf0af65b06b3cac50d73ba437647dc93944f76e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130280"
---
# <a name="imsrdpclient10remoteprogram3-property"></a>IMsRdpClient10：： RemoteProgram3 屬性

支援 [**ITSRemoteProgram3**](itsremoteprogram3.md) 介面的物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_RemoteProgram3(
  [out, retval] ITSRemoteProgram3 **ppRemoteProgram
);
```



## <a name="property-value"></a>屬性值

傳回 [**ITSRemoteProgram3**](itsremoteprogram3.md) 介面指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





