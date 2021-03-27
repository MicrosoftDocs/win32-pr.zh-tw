---
description: 當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。
ms.assetid: f159b829-623c-4348-9692-7317663811a7
title: 'IIdentityChangeNotify：： QuerySwitchIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.QuerySwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 42f8033c943e402d434c973f8c768ed5a951811d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849182"
---
# <a name="iidentitychangenotifyqueryswitchidentities-method"></a>IIdentityChangeNotify：： QuerySwitchIdentities 方法

\[**QuerySwitchIdentities** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

當目前使用者要求切換其使用者身分識別，但在切換之前發生時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT QuerySwitchIdentities();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

參數查詢的結果。 如果應該繼續切換，請返回 \_ [確定]。 否則，會傳回 E \_ 進程 \_ 取消 \_ 的參數，表示應該中止使用者身分識別切換。

## <a name="remarks"></a>備註

當使用者要求切換身分識別時，您可以執行此方法來為您的應用程式提供自訂行為。 您可以藉由傳回「E 進程取消」參數的值，停止暫止的身分識別切換 \_ \_ \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::SwitchIdentities**](iidentitychangenotify-switchidentities.md)
</dt> </dl>

 

 




