---
description: 當使用者身分識別切換時呼叫。
ms.assetid: e88383fc-e58e-4987-be4b-8ce2ab1368db
title: 'IIdentityChangeNotify：： SwitchIdentities 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify.SwitchIdentities
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4b03963f656f84197e6008b5fae33f6ca9f5963ce71959c16cf69ffd68d63d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049751"
---
# <a name="iidentitychangenotifyswitchidentities-method"></a>IIdentityChangeNotify：： SwitchIdentities 方法

\[**SwitchIdentities** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

當使用者身分識別切換時呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT SwitchIdentities();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當使用者已成功切換身分識別時，您可以執行此方法來為您的應用程式提供自訂行為。 若要在發生使用者身分識別切換之前提供自訂行為，請執行 [**IIdentityChangeNotify：： QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/>    | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> <dt>

[**IIdentityChangeNotify::QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)
</dt> </dl>

 

 




