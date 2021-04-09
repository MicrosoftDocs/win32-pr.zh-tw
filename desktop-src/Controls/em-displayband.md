---
title: 'EM_DISPLAYBAND 訊息 (Richedit .h) '
description: 顯示 rich edit 控制項的部分內容，如先前使用 EM FORMATRANGE 訊息針對裝置格式化的部分 \_ 。
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND message Windows 控制項
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934635"
---
# <a name="em_displayband-message"></a>EM \_ DISPLAYBAND 訊息

顯示 rich edit 控制項的部分內容，如先前使用 [**EM \_ FORMATRANGE**](em-formatrange.md) 訊息針對裝置格式化的部分。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構，指定裝置的顯示區域。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為 **TRUE**。

如果作業失敗，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

矩形會裁剪 (COM) 物件的文字和元件物件模型。 應用程式不需要設定裁剪區域。

「群組」是使用一或多個不同的矩形或群組來產生單一輸出頁面的處理常式。 當所有條紋都放在頁面上時，就會產生完整的影像結果。 這種方法通常是由沒有足夠記憶體的點陣印表機，或一次影像一整頁的功能所使用。 條紋裝置包含大部分的點矩陣印表機以及某些雷射印表機。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印 Rich Edit 控制項](printing-rich-edit-controls.md)
</dt> </dl>

 

