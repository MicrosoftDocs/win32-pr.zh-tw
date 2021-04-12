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
ms.openlocfilehash: 334b0cd4e71cb1dde48bd7868a3dbe23fc2a4a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384201"
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
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





