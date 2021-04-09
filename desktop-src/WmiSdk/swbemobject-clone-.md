---
description: '\_SWbemObject 物件的 clone 方法會傳回新的物件，這個物件是目前物件的複本。'
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: 'SWbemObject.Clone_ 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027312"
---
# <a name="swbemobjectclone_-method"></a>SWbemObject 複製 \_ 方法

[**SWbemObject**](swbemobject.md)物件的 **clone \_** 方法會傳回新的物件，這個物件是目前物件的複本。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果成功，這個方法會傳回新的 [**SWbemObject**](swbemobject.md) 物件。

## <a name="error-codes"></a>錯誤碼

完成 **複製 \_** 方法之後， **Err** 物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

未指定 **任何** 參數做為參數，因此在此使用方式中無法接受。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法複製物件。

</dd> </dl>

## <a name="remarks"></a>備註

使用複製方法來複製類別定義或實例。 **\_** 當您在修改新複本時，需要物件的原始複本進行備份時，這非常有用。 同樣地，您也可以使用這個方法，從單一來源實例建立許多新的實例。 例如，您可以使用 [**SWbemObject SpawnInstance \_**](swbemobject-spawninstance-.md)來建立單一起始實例，並使用 **\_ SWbemObject** 來快速產生實例的100複本。 接著，您可以修改物件，並提供每一個特定的值。

您無法使用這個方法將類別定義轉換成實例，或是將實例轉換成類別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




