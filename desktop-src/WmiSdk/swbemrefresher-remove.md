---
description: SWbemRefresher 方法會從複習中移除具有指定索引的 SWbemRefreshableItem 物件。
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: 'SWbemRefresher： Remove 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945676"
---
# <a name="swbemrefresherremove-method"></a>SWbemRefresher 方法

**SWbemRefresher** 方法會從複習中移除具有指定索引的 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件。 **SWbemRefreshableItem** 物件可以是單一物件或物件集。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*LIndex* 
</dt> <dd>

[**SWbemRefresher**](swbemrefresher.md)物件中專案的索引。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

旗標必須設定為 t0 (零) 。

</dd> <dt>

*objWbemNamedvalueSet* \[選\]
</dt> <dd>

Null。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法沒有傳回值。

## <a name="remarks"></a>備註

**錯誤碼** 如果重新整理程式沒有具有指定之索引的專案，就會產生 **wbemErrNotFound** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




