---
title: 點擊測試選項
description: 此區段會列出與 HitTestThemeBackground 函數的 >dwoptions 參數搭配使用的選項值。 如需指定其中一個選項時所傳回值的清單，請參閱點擊測試傳回值。
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462233"
---
# <a name="hit-test-options"></a>點擊測試選項

此區段會列出與 [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground)函數的 *>dwoptions* 參數搭配使用的選項值。 如需指定其中一個選項時所傳回值的清單，請參閱 [點擊測試傳回值](theme-hit-test-retval.md)。

## <a name="option-values"></a>選項值

下表列出點擊測試選項。



| 選項                       | 值                                                                                                                    | 描述                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | 主題背景區段點擊測試選項。                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | 固定框線點擊測試選項。                                                                                                                                                       |
| HTTB \_ 標題                | 0x00000004                                                                                                               | 標題點擊測試選項。                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         |  (HTTB \_ RESIZINGBORDER \_ LEFT \| HTTB \_ RESIZINGBORDER \_ TOP \| HTTB \_ RESIZINGBORDER \_ RIGHT \| HTTB \_ RESIZINGBORDER \_ 下)  | 調整框線點擊測試選項的大小。                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ 左方   | 0x00000010                                                                                                               | 調整左方框線點擊測試選項的大小。                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ TOP    | 0x00000020                                                                                                               | 調整上方框線點擊測試選項的大小。                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | 0x00000040                                                                                                               | 調整右框線點擊測試選項的大小。                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ 底部 | 0x00000080                                                                                                               | 調整下方框線點擊測試選項的大小。                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | 調整框線的大小會指定為範本，而不只是視窗邊緣。 此選項與 HTTB \_ SYSTEMSIZINGMARGINS 互斥;HTTB \_ SIZINGTEMPLATE 優先。         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | 使用系統調整框線寬度，而非視覺化樣式內容邊界。 此選項與 HTTB \_ SIZINGTEMPLATE 互斥;HTTB \_ SIZINGTEMPLATE 優先。 |



 

 

 




