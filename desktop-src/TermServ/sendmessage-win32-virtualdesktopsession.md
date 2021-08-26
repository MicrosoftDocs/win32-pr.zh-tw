---
title: Win32_VirtualDesktopSession 類別的 SendMessage 方法
description: 透過虛擬桌面會話傳送訊息給使用者。
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage 方法遠端桌面服務
- SendMessage 方法遠端桌面服務，Win32_VirtualDesktopSession 類別
- Win32_VirtualDesktopSession 類別遠端桌面服務，SendMessage 方法
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159d9c8b4e8c4b5086fff9c4fc6c67c0a6e33464eeefee77d15a620b157bd55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988148"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Win32 VirtualDesktopSession 類別的 SendMessage 方法 \_

透過虛擬桌面會話傳送訊息給使用者。

## <a name="syntax"></a>語法


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*標題* \[在\]
</dt> <dd>

訊息的標題。

</dd> <dt>

*訊息* \[在\]
</dt> <dd>

訊息的內容。

</dd> </dl>

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

 

 





