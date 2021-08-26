---
description: 通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: 'ITipAutocompleteClient：： UserSelection 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2dac765c3f1c3e709bb7066a1645c2d77783ea555bccd81f9d5809da802d7043
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843478"
---
# <a name="itipautocompleteclientuserselection-method"></a>ITipAutocompleteClient：： UserSelection 方法

通知輸入面板，使用者已在自動完成清單中選取某個內容，並捨棄尚未插入的所有剩餘文字。

## <a name="syntax"></a>語法


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | 描述                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

從提供者呼叫這個方法，以通知用戶端已由使用者進行選取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITipAutocompleteClient 介面**](itipautocompleteclient.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




