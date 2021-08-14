---
title: 時間限制
description: 時間限制
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- CAPTUREPARMS 結構
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
- CAPTUREPARMS 結構
- WM_CAP_SET_SEQUENCE_SETUP 訊息
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6211edf3ce3fb86b4c0430c685ff05ff7f95c718c0a89e7ba782ae342feb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801262"
---
# <a name="time-limit"></a>時間限制

您可以使用 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fLimitEnabled** 和 **wTimeLimit** 成員來限制捕捉作業的持續時間。 **FLimitEnabled** 成員會指出是否要計時捕捉作業，而 **wTimeLimit** 則會指定捕捉作業的最長持續時間。

您可以使用 **fLimitEnabled** 和 **wTimeLimit** 的值，方法是使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) 。 您可以藉由指定 **TRUE** 作為 **fLimitEnabled** 的值來啟用捕捉作業的計時器，也可以指定 **wTimeLimit** 的值（以秒為單位）來設定捕捉作業的持續時間。 設定這些成員之後，請使用 [ [**WM \_ CAP \_ set \_ SEQUENCE \_ SETUP**](wm-cap-set-sequence-setup.md) message (或 [**CapCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)宏) ，將更新的 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構傳送至 [捕獲] 視窗。 **FLimitEnabled** 的預設值為 **FALSE**。

 

 




