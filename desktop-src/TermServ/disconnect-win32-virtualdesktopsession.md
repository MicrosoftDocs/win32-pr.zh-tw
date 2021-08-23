---
title: Win32_VirtualDesktopSession 類別的中斷連接方法
description: 中斷虛擬桌面會話的連線。
ms.assetid: 9dbb256c-c416-4749-87be-05a906070560
ms.tgt_platform: multiple
keywords:
- 中斷連接方法遠端桌面服務
- 中斷連接方法遠端桌面服務，Win32_VirtualDesktopSession 類別
- Win32_VirtualDesktopSession 類別遠端桌面服務，中斷連線方法
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Disconnect
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998e6dad97c1dcf6e55a999f02eac34a9881efa27c6cb6636f729cbb75befad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515658"
---
# <a name="disconnect-method-of-the-win32_virtualdesktopsession-class"></a>Win32 VirtualDesktopSession 類別的 Disconnect 方法 \_

中斷虛擬桌面會話的連線。

## <a name="syntax"></a>語法


```mof
uint32 Disconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ VirtualDesktopSession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





