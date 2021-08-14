---
description: '\_SWbemLastError 物件的 clone 方法會傳回新的物件，這個物件是目前 SWbemLastError 物件的複製。'
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: 'SWbemLastError.Clone_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314664"
---
# <a name="swbemlasterrorclone_-method"></a>SWbemLastError 複製 \_ 方法

[**SWbemLastError**](swbemlasterror.md)物件的 **clone \_** 方法會傳回新的物件，這個物件是目前 **SWbemLastError** 物件的複製。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果 **複製 \_** 方法成功，它會傳回新的 [**SWbemLastError**](swbemlasterror.md)物件。

## <a name="error-codes"></a>錯誤碼

**複製 \_** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> </dl>

## <a name="remarks"></a>備註

使用複製方法來複製類別定義或實例。 **\_** 當您需要在修改新的複本時，備份物件的原始複本時，這個方法很有用。 此外，也可以使用這個方法，從單一來源實例建立許多新的實例。 例如，使用 [**SWbemObject SpawnInstance \_**](swbemobject-spawninstance-.md)來建立單一起始實例，並使用 **\_ SWbemLastError** 來快速產生實例的100複本。 接著，您可以修改物件，並將特定的值提供給每個物件。

您無法使用這個方法將類別定義轉換成實例，或是將實例轉換成類別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




