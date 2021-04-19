---
description: 取得標記之未附加參考的 XML 格式。
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken：： TokenReferenceUnattached 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966731"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a>IUpdateEndpointAuthToken：： TokenReferenceUnattached 方法

取得標記之未附加參考的 XML 格式。

## <a name="syntax"></a>語法


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszTokenReference* \[擴展\]
</dt> <dd>

未附加之標記參考的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。 否則，會傳回 COM 或 Windows 錯誤碼。

## <a name="remarks"></a>備註

未附加的參考參考了 referece (，例如使用權杖) 的 signiture，而該權杖不在標記所在的訊息中。

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

 

 




