---
title: 影片緩衝區
description: 影片緩衝區
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687688"
---
# <a name="video-buffers"></a>影片緩衝區

搭配影片捕獲使用的緩衝區位於記憶體堆積中。 捕捉作業中所使用的緩衝區數目可能會不同，而且取決於 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **wNumVideoRequested** 成員和可用系統記憶體的值。

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來抓取要求的視訊緩衝區目前的值。 目前要求的影片緩衝區數目會儲存在 **CAPTUREPARMS** 結構的 **wNumVideoRequested** 成員中。 您可以藉由更新這個成員來要求緩衝區的位置和數目，然後使用 [ [**WM \_ CAP \_ SET \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。

 

 




