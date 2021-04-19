---
description: SWbemRefresher 加入方法會將新的 SWbemRefreshableItem 物件加入至 SWbemRefresher 物件中的集合。SWbemRefreshableItem 物件至 SWbemRefresher 物件中的集合。
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: 'SWbemRefresher： Add 方法 (>wbemdisp.tlb. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981069"
---
# <a name="swbemrefresheradd-method"></a>SWbemRefresher 新增方法

**SWbemRefresher 加入** 方法會將新的 [**SWbemRefreshableItem**](swbemrefreshableitem.md)物件加入至 [**SWbemRefresher**](swbemrefresher.md)物件中的集合。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objWbemService* 
</dt> <dd>

必要。 代表命名空間之連接的 [**SWbemServices**](swbemservices.md) 物件，在此命名空間中新增到重新整理程式的物件。

</dd> <dt>

*strInstancePath* 
</dt> <dd>

必要。 包含命名空間中物件之相對路徑的字串。 路徑必須包含實例。 傳回之 [**SWbemRefreshableItem**](swbemrefreshableitem.md)的 [**index**](swbemrefreshableitem-index.md)屬性代表重新整理程式集合中的物件索引。

</dd> <dt>

*iFlags* \[選\]
</dt> <dd>

字串，包含執行方法之物件的物件路徑。

</dd> <dt>

*objWbemNamedvalueSet* \[選\]
</dt> <dd>

一般而言，這是未定義的。 否則，這會是 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 物件，其專案代表服務要求的提供者可使用的內容資訊。 支援或需要這類資訊的提供者，必須記錄已辨識的值名稱、值的資料類型、允許的值，以及語義。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功，則會傳回包含單一可重新整理物件的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。

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

 

 




