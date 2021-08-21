---
description: 應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列出的手勢時，如何處理 UI 意見反應。
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: '手勢視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f572addf2ad7a98dbe3afc63c69a305ea15546e9533918d952271372cf52b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849817"
---
# <a name="gesture-visualization"></a>手勢視覺效果

應用程式或 UI 架構會使用下列常數，識別當偵測到其中一個所列出的手勢時，如何處理 UI 意見反應。

這些常數會搭配 **spi \_ GETGESTUREVISUALIZATION** 和 **Spi \_ SETGESTUREVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。

**注意**  

若要取得或設定畫筆視覺效果資訊，建議您使用 **spi \_ GETPENVISUALIZATION** 和 **spi \_ SETPENVISUALIZATION** 參數，以及在 [ [**畫筆視覺效果**](pen-visualization.md)] 中列出的常數。

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ 關閉**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



指定所有手勢的 UI 意見反應都是 off。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ 于**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



指定所有手勢的 UI 意見反應都是開啟的。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ 分流**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



指定點擊的 UI 意見反應。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



指定點兩下的 UI 意見反應。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



指定按下和點的 UI 回饋。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



指定按下並按住的 UI 意見反應。


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



指定以滑鼠右鍵按一下的 UI 意見反應。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                 |
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

 

