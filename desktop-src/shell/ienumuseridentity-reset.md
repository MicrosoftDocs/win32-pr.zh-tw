---
description: 重設列舉中已抓取介面的內部計數。
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'IEnumUserIdentity：： Reset 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192678"
---
# <a name="ienumuseridentityreset-method"></a>IEnumUserIdentity：： Reset 方法

\[**IEnumUserIdentity：： Reset** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

重設列舉中已抓取介面的內部計數。

## <a name="syntax"></a>語法


```C++
HRESULT Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。 呼叫這個方法將會重設此計數的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity：： Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity：： GetCount**](ienumuseridentity-getcount.md)
</dt> <dt>

[**IEnumUserIdentity：： Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




