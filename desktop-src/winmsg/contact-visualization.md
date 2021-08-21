---
description: 應用程式或 UI 架構會使用下列常數，來識別偵測到輸入連絡人時如何處理 UI 意見反應。
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: '連絡人視覺效果 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437251"
---
# <a name="contact-visualization"></a>連絡人視覺效果

應用程式或 UI 架構會使用下列常數，來識別偵測到輸入連絡人時如何處理 UI 意見反應。

這些常數會搭配 **spi \_ GETCONTACTVISUALIZATION** 和 **Spi \_ SETCONTACTVISUALIZATION** 參數和 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 函式使用。

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ 關閉**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



指定所有連絡人的 UI 意見反應都是 off。


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ 于**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



指定所有連絡人的 UI 回饋。


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



使用簡報模式視覺效果，指定所有連絡人的 UI 意見反應。


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

[**手勢視覺效果**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[輸入意見設定](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

