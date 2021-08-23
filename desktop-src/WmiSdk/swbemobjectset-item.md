---
description: Swbemobjectset 搭配使用物件的 Item 方法會從集合取得 SWbemObject。
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857218"
---
# <a name="swbemobjectsetitem-method"></a>Swbemobjectset 搭配使用專案方法

[**Swbemobjectset 搭配使用**](swbemobjectset.md)物件的 **Item** 方法會從集合取得 [**SWbemObject**](swbemobject.md) 。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*strObjectPath* 
</dt> <dd>

必要。 要從集合中取出之物件的相對路徑。 範例： Win32 \_ LogicalDisk = "C："

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，要求的 [**SWbemObject**](swbemobject.md) 物件就會傳回。

## <a name="error-codes"></a>錯誤碼

當 **專案** 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。

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

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的專案。

</dd> </dl>

## <a name="remarks"></a>備註

**Item** 方法可能需要很多的處理器時間，因為必須由集合的元素提供者完成列舉，才能傳回結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbemobjectset 搭配使用<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




