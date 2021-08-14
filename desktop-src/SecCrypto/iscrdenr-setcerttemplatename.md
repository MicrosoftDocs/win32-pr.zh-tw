---
description: 指定憑證範本的名稱。
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: ISCrdEnr：： setCertTemplateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993038"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>ISCrdEnr：： setCertTemplateName 方法

**SetCertTemplateName** 方法會指定憑證範本的名稱。

## <a name="syntax"></a>語法


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，決定是否要設定憑證範本的真實名稱或顯示名稱。 如果 *dwFlags* 的值為捨棄 \_ 註冊 \_ \_ 憑證範本 \_ 顯示 \_ 名稱，則會設定憑證範本的顯示名稱。 否則，會設定憑證範本的真實名稱。

</dd> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

將在憑證要求中使用的憑證範本名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

## <a name="remarks"></a>備註

如果您未藉由呼叫 **ISCrdEnr：： setCertTemplateName** 來設定憑證範本名稱，則名稱會預設為可用憑證範本清單中的第一個名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




