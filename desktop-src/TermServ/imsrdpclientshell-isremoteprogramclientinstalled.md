---
title: IMsRdpClientShell IsRemoteProgramClientInstalled 屬性
description: 抓取遠端桌面連線 (RDC) 用戶端是否支援 Windows Server 2008 R2 RemoteApp 功能。
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- IsRemoteProgramClientInstalled 屬性遠端桌面服務
- IsRemoteProgramClientInstalled 屬性遠端桌面服務，IMsRdpClientShell 介面
- IMsRdpClientShell 介面遠端桌面服務，IsRemoteProgramClientInstalled 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094219"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>IMsRdpClientShell：： IsRemoteProgramClientInstalled 屬性

抓取遠端桌面連線 (RDC) 用戶端是否支援 Windows Server 2008 R2 RemoteApp 功能。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>屬性值

抓取遠端桌面連線 (RDC) 用戶端是否支援 RemoteApp 功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





