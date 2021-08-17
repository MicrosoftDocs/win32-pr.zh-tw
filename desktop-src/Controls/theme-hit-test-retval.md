---
title: 點擊測試傳回值
description: 此區段會列出在 HitTestThemeBackground 函數的 pwHitTestCode 參數中傳回的點擊測試程式碼值。
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020765e6f766efc2c79e869a1b06cfceac2c13a451cc381d88ae066cc1478c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797598"
---
# <a name="hit-test-return-values"></a>點擊測試傳回值

此區段會列出在 [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground)函數的 *pwHitTestCode* 參數中傳回的點擊測試程式碼值。 傳回的程式碼值取決於 **HitTestThemeBackground** 函數的 *>dwoptions* 參數中指定的點擊測試選項。 如需選項的清單，請參閱 [點擊測試選項](theme-hit-test-options.md)。

## <a name="return-values"></a>傳回值

下表列出點擊測試選項和對應的傳回碼。



| 選項                       | 傳回碼  | 描述                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | 底部框線區段中的點擊測試成功。                                                                   |
|                              | HTBOTTOMLEFT  | 底部和左邊框線交集的點擊測試成功。                                                     |
|                              | HTBOTTOMRIGHT | 點擊率測試成功于右下角框線交集。                                                    |
|                              | HTCLIENT      | 中間背景區段的點擊測試成功。                                                               |
|                              | HTLEFT        | 左邊框線區段中的點擊測試成功。                                                                     |
|                              | HTNOWHERE     | 點擊測試在控制項之外或在透明區域上成功。                                                   |
|                              | HTRIGHT       | 右框線區段中的點擊測試成功。                                                                    |
|                              | HTTOP         | 頂端框線區段中的點擊測試成功。                                                                      |
|                              | HTTOPLEFT     | 點擊測試成功于左上和左框線交集。                                                            |
|                              | HTTOPRIGHT    | 點擊率測試成功于右上角框線交集。                                                       |
| HTTB \_ 標題                | HTCAPTION     | 點擊測試成功于頂端、左上角或右上角的背景區段。                                         |
|                              | HTNOWHERE     | 點擊測試在控制項之外或在透明區域上成功。                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | 在中間背景區段以外的任何背景區段中，點擊測試成功。                                 |
|                              | HTCLIENT      | 中間背景區段的點擊測試成功。                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | 在中間背景區段中進行點擊測試失敗，並調整區域大小，但在背景框線區段中成功。 |
| HTTB \_ RESIZINGBORDER \_ 底部 | HTBOTTOM      | 底部框線區段中的點擊測試成功。                                                                   |
| HTTB \_ RESIZINGBORDER \_ 左方   | HTLEFT        | 左邊框線區段中的點擊測試成功。                                                                     |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | HTRIGHT       | 右框線區段中的點擊測試成功。                                                                    |
| HTTB \_ RESIZINGBORDER \_ TOP    | HTTOP         | 頂端框線區段中的點擊測試成功。                                                                      |



 

 

 




