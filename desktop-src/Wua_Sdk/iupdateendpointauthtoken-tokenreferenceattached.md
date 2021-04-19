---
description: 取得 token 之附加參考的 XML 格式。
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'IUpdateEndpointAuthToken：： TokenReferenceAttached 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966732"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a>IUpdateEndpointAuthToken：： TokenReferenceAttached 方法

取得 token 之附加參考的 XML 格式。

## <a name="syntax"></a>語法


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszTokenReference* \[擴展\]
</dt> <dd>

附加的 token 參考的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。 否則，會傳回 COM 或 Windows 錯誤碼。

## <a name="remarks"></a>備註

附加的參考會參考 referece (例如，使用權杖的 signiture) 位於權杖所在的相同訊息中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>                |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>UpdateEndpointAuth .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUpdateEndpointAuthToken**](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




