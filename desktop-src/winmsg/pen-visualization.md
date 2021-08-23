---
description: 應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列的畫筆手勢時，如何處理 UI 意見反應。
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: '畫筆視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60b9f75493a361cc167b65fba1783bc01f909d76211b1076e2faccc2e6f00116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548488"
---
# <a name="pen-visualization"></a>畫筆視覺效果

應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列的畫筆手勢時，如何處理 UI 意見反應。

這些常數會搭配 **spi \_ GETPENVISUALIZATION** 和 **Spi \_ SETPENVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ 關閉**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



指定所有畫筆手勢的 UI 回饋都是 off。


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ 于**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



指定所有畫筆手勢的 UI 意見反應都是開啟的。


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ 分流**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



指定畫筆點擊的 UI 意見反應。


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



指定畫筆點兩下的 UI 意見反應。


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION 資料 \_ 指標**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



指定畫筆游標的 UI 意見反應。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定常數](configuration-constants.md)
</dt> <dt>

[**連絡人視覺效果**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[輸入意見設定](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

