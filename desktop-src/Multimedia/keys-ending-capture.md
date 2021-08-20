---
title: 金鑰結束捕獲
description: 金鑰結束捕獲
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140048"
---
# <a name="keys-ending-capture"></a>金鑰結束捕獲

您可以允許使用者在鍵盤上按下按鍵或按鍵組合，或按滑鼠右鍵或滑鼠左鍵，以中止捕捉會話。 如果使用者中止即時捕獲會話，則會捨棄 capture 檔案的內容。 如果使用者中止步驟框架捕獲會話，則會儲存捕捉檔案的內容，直到中止捕獲為止。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得中止捕捉會話的設定。 目前的按鍵設定會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **vKeyAbort** 成員中;目前的滑鼠設定會儲存在 **fAbortLeftMouse** 和 **fAbortRightMouse** 成員中。 您可以設定新的按鍵或按鍵組合，方法是指定 keycode 或 keycode 組合 (如 CTRL 或 SHIFT 鍵組合) 為 **vKeyAbort** 的值，或是藉由指定 **fAbortLeftMouse** 或 **fAbortRightMouse** 成員，將滑鼠左鍵或右鍵設定為中止索引鍵。 設定這些成員之後，請使用 [ [**WM \_ CAP \_ set \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md) message (或 [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。 **VKeyAbort** 的預設值為 VK \_ ESCAPE。 您必須先呼叫 [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函數，然後再指定可中止捕捉會話的按鍵。 **FAbortLeftMouse** 和 **fAbortRightMouse** 的預設值為 **TRUE**。

 

 