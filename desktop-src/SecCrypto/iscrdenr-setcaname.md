---
description: 指定 (CA) 的憑證授權單位單位名稱。
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: ISCrdEnr：： setCAName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988953"
---
# <a name="iscrdenrsetcaname-method"></a>ISCrdEnr：： setCAName 方法

**SetCAName** 方法會指定 (CA) 的 [*憑證授權單位*](../secgloss/c-gly.md)單位名稱。

## <a name="syntax"></a>語法


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

值，指定名稱是指 CA 名稱或 CA 的電腦名稱稱。 如果此值為捨棄 \_ 註冊 \_ CA \_ 電腦 \_ 名稱 (定義為 0x01) ，則名稱會參考 CA 的電腦名稱稱。 否則，名稱會參考 CA 名稱。

</dd> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

憑證範本的名稱。

</dd> <dt>

*bstrCAName* \[在\]
</dt> <dd>

要與 *bstrCertTemplateName* 所指定的憑證範本搭配使用的 CA 名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="vb"></a>VB

傳回值是 **HRESULT**。 S 的值 \_ 表示呼叫成功。

## <a name="remarks"></a>備註

使用這個方法來指定憑證範本的 CA。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
