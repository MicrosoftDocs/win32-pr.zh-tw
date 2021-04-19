---
description: 允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。
ms.assetid: c82ffecb-f3e6-4c50-80bb-8393b39d3b2a
title: 'ITipAutocompleteClient：:P referredRects 方法 (TipAutoComplete .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.PreferredRects
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 04e935c668e858ae3d22936e8a63f9116ebd6ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984629"
---
# <a name="itipautocompleteclientpreferredrects-method"></a>ITipAutocompleteClient：:P referredRects 方法

允許用戶端建議在何處放置自動完成清單，以避免重迭輸入面板。

## <a name="syntax"></a>語法


```C++
HRESULT PreferredRects(
  [in]      RECT *prcACList,
  [in]      RECT *prcField,
  [out]     RECT *prcModified,
  [in, out] BOOL *pfShownAboveTip
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prcACList* \[在\]
</dt> <dd>

以螢幕座標表示提供者慣用位置和自動完成清單使用者介面大小的矩形。

</dd> <dt>

*prcField* \[在\]
</dt> <dd>

螢幕座標中的矩形，指出焦點欄位的位置和大小。

</dd> <dt>

*prcModified* \[擴展\]
</dt> <dd>

以目前的提示狀態和慣用的自動完成清單位置和 *prcACList* 指定的大小為基礎的矩形。

</dd> <dt>

*pfShownAboveTip* \[in、out\]
</dt> <dd>

如果修改的矩形要顯示在文字輸入面板的目的地區域上方，則為 **TRUE** ;否則 **為 FALSE**。 在呼叫方法之前，必須將這個值初始化為提供者的慣用方向。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 呼叫 [**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md) ，在呼叫 [**ITipAutocompleteClient：:P referredrects 方法**](itipautocompleteclient-preferredrects.md)之前，設定快顯視窗自動完成清單視窗。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 發生未指定的錯誤。<br/>                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>備註

這是自動完成提供者在即將顯示自動完成使用者介面時所呼叫的方法。 用戶端會修改 *prcACList* 透過 *prcModified* 引數所指定的提供者慣用矩形。

呼叫 [**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md) ，在呼叫 **PreferredRects** 之前，設定快顯自動完成清單視窗控制碼。 若未這麼做，將會在呼叫 **PreferredRects** 時造成 **E \_ INVALIDARG** 錯誤。

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

[**ITipAutocompleteClient：： RequestShowUI 方法**](itipautocompleteclient-requestshowui.md)
</dt> <dt>

[文字輸入面板參考](text-input-panel-reference.md)
</dt> </dl>

 

 




