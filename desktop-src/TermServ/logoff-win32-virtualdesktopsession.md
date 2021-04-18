---
title: 'Win32_VirtualDesktopSession 類別的登出方法 (Sensevts) '
description: 登出虛擬桌面會話的使用者。
ms.assetid: a9c90ace-324c-4eec-86e1-30ce35307e52
ms.tgt_platform: multiple
keywords:
- 登出方法遠端桌面服務
- 登出方法遠端桌面服務，Win32_VirtualDesktopSession 類別
- Win32_VirtualDesktopSession 類別遠端桌面服務，登出方法
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Logoff
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4582744f0d8ba9300bd620a45190ec1de4819ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384970"
---
# <a name="logoff-method-of-the-win32_virtualdesktopsession-class"></a>Win32 VirtualDesktopSession 類別的登出方法 \_

登出虛擬桌面會話的使用者。

## <a name="syntax"></a>語法


```mof
uint32 Logoff();
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
| 標頭<br/>                   | <dl> <dt>Sensevts。h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ VirtualDesktopSession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





