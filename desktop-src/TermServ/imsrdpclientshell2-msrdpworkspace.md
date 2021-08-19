---
title: IMsRdpClientShell2 MsRdpWorkspace 屬性
description: 抓取 IMsRdpWorkspace 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- MsRdpWorkspace 屬性遠端桌面服務
- MsRdpWorkspace 屬性遠端桌面服務，IMsRdpClientShell2 介面
- IMsRdpClientShell2 介面遠端桌面服務，MsRdpWorkspace 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854432"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2：： MsRdpWorkspace 屬性

抓取 [**IMsRdpWorkspace**](imsrdpworkspace.md) 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>屬性值

[**IMsRdpWorkspace**](imsrdpworkspace.md)介面指標的位址。

## <a name="remarks"></a>備註

[**IMsRdpWorkspace**](imsrdpworkspace.md)介面不會公開為自訂介面。 它只能透過 [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) 方法來存取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

