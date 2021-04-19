---
description: 傳回 (Ca 的憑證授權單位單位數目) 願意根據指定的憑證範本頒發證書。
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: ISCrdEnr：： getCACount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998537"
---
# <a name="iscrdenrgetcacount-method"></a>ISCrdEnr：： getCACount 方法

**GetCACount** 方法會傳回 (ca 的 [*憑證授權單位*](../secgloss/c-gly.md)單位數目) 願意根據指定的憑證範本頒發證書。

## <a name="syntax"></a>語法


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrCertTemplateName* \[在\]
</dt> <dd>

表示憑證範本名稱的字串。

</dd> <dt>

*pdwCACount* \[擴展\]
</dt> <dd>

**LONG** 的指標，傳回將為 *bstrCertTemplateName* 中指定的憑證範本發出憑證的可用 ca 數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

### <a name="c"></a>C++

如果方法成功，則方法會傳回 S \_ OK。

如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。 如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。

### <a name="vb"></a>VB

**Long** 值，代表將為 *bstrCertTemplateName* 中指定的憑證範本發出憑證的可用 ca 數目。

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

 

 
