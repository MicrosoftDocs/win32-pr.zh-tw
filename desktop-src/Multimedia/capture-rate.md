---
title: 捕捉速率
description: 捕捉速率
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691658"
---
# <a name="capture-rate"></a>捕捉速率

「捕獲速率」是每秒在捕獲會話中所捕獲的框架數目。 您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得目前的捕獲速度。 目前的捕獲速率會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **dwRequestMicroSecPerFrame** 成員中。 您可以藉由指定連續框架與此成員的值之間的微秒數來設定捕捉速率，然後使用 [ [**WM \_ CAP \_ set \_ SEQUENCE 設定 \_**](wm-cap-set-sequence-setup.md)訊息 (] 或 [ [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ] 宏) ，將更新的 **CAPTUREPARMS** 結構傳送至 [捕獲] 視窗。 **DwRequestMicroSecPerFrame** 的預設值是66667，對應至每秒15個畫面格。

 

 




