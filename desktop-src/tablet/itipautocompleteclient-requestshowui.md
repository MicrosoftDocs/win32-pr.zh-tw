---
description: 決定輸入面板是否已準備好顯示自動完成清單。
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'ITipAutocompleteClient：： RequestShowUI 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193151"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>ITipAutocompleteClient：： RequestShowUI 方法

決定輸入面板是否已準備好顯示自動完成清單。

## <a name="syntax"></a>語法


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWndACList* \[在\]
</dt> <dd>

自動完成清單使用者介面的視窗控制碼。

</dd> <dt>

*pfAllowShowing* \[擴展\]
</dt> <dd>

如果用戶端建議不要顯示自動完成清單使用者介面，則 **為 FALSE** 。 如果自動完成提供者可以顯示清單使用者介面，**則為 TRUE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="remarks"></a>備註

當自動完成提供者即將顯示自動完成使用者介面時，會呼叫這個方法。 如果用戶端的內部狀態不允許提供者顯示使用者介面， *pfAllowShowing* 會設為 **FALSE**。 例如，當文字從 Tablet PC 輸入面板上的手寫面板傳送至欄位，且使用者立即開始筆墨時，用戶端將不會建議顯示自動完成使用者介面，藉由將 *pfAllowShowing* 設定為 **FALSE**，以避免 destructing 使用者的筆跡。

呼叫 **RequestShowUI** ，在呼叫 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)之前，先設定 popup 自動完成清單視窗控制碼。 若未這麼做，將會在呼叫 **PreferredRects** 時造成 **E \_ INVALIDARG** 錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                                       |
| 標頭<br/>                   | <dl> <dt>TipAutoComplete (也需要 Peninputpanel \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITipAutocompleteClient 介面**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient：:P referredRects 方法**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




