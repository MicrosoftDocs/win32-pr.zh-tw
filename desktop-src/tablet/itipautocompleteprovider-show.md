---
description: 顯示或隱藏自動完成清單。
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'ITipAutocompleteProvider：： Show 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2afc5fc264df4d38e85dfa3374714b06908eee8ec1c5517b49dc32cbcbd44f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716448"
---
# <a name="itipautocompleteprovidershow-method"></a>ITipAutocompleteProvider：： Show 方法

顯示或隱藏自動完成清單。

## <a name="syntax"></a>語法


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fShow* \[在\]
</dt> <dd>

**TRUE** 表示顯示自動完成使用者介面， **FALSE** 則會隱藏自動完成清單使用者介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | 描述                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

用戶端會呼叫這個方法來顯示或隱藏自動完成清單。 如果未顯示自動完成清單，且 *fShow* 為 **FALSE**，則這個方法不會執行任何動作。 如果顯示自動完成清單，且 *fShow* 為 **TRUE**，則這個方法不會執行任何動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITipAutocompleteProvider 介面**](itipautocompleteprovider.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




