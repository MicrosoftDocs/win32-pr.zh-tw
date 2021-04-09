---
title: 'EM_SETTYPOGRAPHYOPTIONS 訊息 (Richedit .h) '
description: 設定 rich edit 控制項之印刷樣式選項的目前狀態。
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934541"
---
# <a name="em_settypographyoptions-message"></a>EM \_ SETTYPOGRAPHYOPTIONS 訊息

設定 rich edit 控制項之印刷樣式選項的目前狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定下列其中一個或兩個值。



| 值                                                                                                                                                                                    | 意義                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**至 \_ADVANCEDTYPOGRAPHY**</dt> </dl> | 已開啟先進的換行和行格式。 <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**\_SIMPLELINEBREAK**</dt> </dl>             | 更快速地細分簡單文字 (需要 **\_ ADVANCEDTYPOGRAPHY**) 。 <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

由 *wParam* 中的一或多個旗標所組成的遮罩。 只會設定或清除此遮罩中設定的旗標。 這可讓您設定或清除單一旗標，而不需要讀取目前的旗標狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *wParam* 有效，**則傳回 TRUE** ，否則傳回 **FALSE**。

## <a name="remarks"></a>備註

Rich edit 控制項會在需要時自動開啟 Advanced line 斷線，例如處理阿拉伯文和希伯來文等複雜字集，以及數學。 它也需要對齊段落、斷字和其他印刷樣式功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETTYPOGRAPHYOPTIONS**](em-gettypographyoptions.md)
</dt> </dl>

 

 





