---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: 'PenInputPanel. InputFailed 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934758"
---
# <a name="peninputpanelinputfailed-event"></a>PenInputPanel. InputFailed 事件

已取代。 [**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。

在 [**PenInputPanel**](peninputpanel-class.md) 物件能夠將使用者輸入插入附加控制項之前變更輸入焦點時發生。

## <a name="syntax"></a>語法


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

叫用 [**PenInputPanel**](peninputpanel-class.md) 物件之控制項的視窗控制碼。

</dd> <dt>

*金鑰* \[在\]
</dt> <dd>

對應到所按下之索引鍵的虛擬機器碼。

</dd> <dt>

*文字* \[在\]
</dt> <dd>

當引發 **InputFailed** 事件時，要插入 *hWnd* 參數所代表之控制項中的字串。

如需 BSTR 資料類型的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> <dt>

*ShiftKey* \[在\]
</dt> <dd>

鍵盤修飾詞的狀態，包括 SHIFT、CAPS、CTRL 和 ALT。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當輸入焦點在使用者輸入插入附加控制項之前變更時，就會發生 **InputFailed** 事件。 例如，如果使用者在書寫板中輸入筆墨，然後在辨識器有機會完成之前先點擊另一個編輯控制項，就會引發此事件。

使用傳遞至這個事件的視窗控制碼，您可以選擇在發生這個事件時，自行插入文字。

> [!Note]  
> 從 Microsoft Windows XP Tablet PC Edition 2005 開始， **InputFailed** 活動不再適用。 文字一律會在焦點變更之前插入。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




