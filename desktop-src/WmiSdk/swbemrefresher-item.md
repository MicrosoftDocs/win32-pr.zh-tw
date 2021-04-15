---
description: SWbemRefresher 方法會從集合傳回指定的 SWbemRefreshableItem。從集合 SWbemRefreshableItem。
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: 'SWbemRefresher 專案方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104195734"
---
# <a name="swbemrefresheritem-method"></a>SWbemRefresher 專案方法

**SWbemRefresher** 方法會從集合傳回指定的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

## <a name="syntax"></a>語法


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* 
</dt> <dd>

集合中專案的索引值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果呼叫成功，則會傳回指定的 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。

## <a name="error-codes"></a>錯誤碼

如果重新整理程式沒有具有指定之索引的專案，就會產生 **wbemErrNotFound** 。

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

 

 




