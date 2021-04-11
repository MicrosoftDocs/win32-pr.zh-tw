---
description: 由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'ITipAutocompleteProvider：： UpdatePendingText 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027548"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>ITipAutocompleteProvider：： UpdatePendingText 方法

由自動完成用戶端用來通知應用程式使用者已筆跡輸入面板中的文字。

## <a name="syntax"></a>語法


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrPendingText* \[在\]
</dt> <dd>

要用來產生自動完成清單的來源文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

此文字不會包含已在焦點欄位中插入的文字。 自動完成提供者負責將目前的欄位文字和選取範圍納入考慮，以產生自動完成清單。 當 *bstrPendingText* 為 **Null** 時，就會使用欄位中選取範圍的目前文字來產生自動完成清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITipAutocompleteProvider 介面**](itipautocompleteprovider.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




