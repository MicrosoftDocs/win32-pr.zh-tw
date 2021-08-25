---
title: User-Initiated Capture
description: User-Initiated Capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP 訊息
- capCaptureGetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca015726aabe7c171f37590a98e60774c34a09c219ef445af3e30f199d5030b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892448"
---
# <a name="user-initiated-capture"></a>User-Initiated Capture

您可以使用 [ [**WM \_ CAP \_ GET \_ SEQUENCE \_ 設定**](wm-cap-get-sequence-setup.md) 訊息 (] 或 [ [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 宏) ，來取得使用者起始之捕獲旗標的目前值。 旗標的值會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms)結構的 **fMakeUserHitOKToCapture** 成員中。 您可以藉由將這個成員設定為 **TRUE**，讓使用者精確控制開始抓取會話的時間。 AVICap 會在配置 capture 會話的所有影片和音訊緩衝區之後顯示對話方塊。 這可讓使用者因軟體初始化而排除捕獲延遲。 如果您的應用程式使用少量的影片緩衝區，則可能不需要這個對話方塊。 預設值為 **FALSE**。

 

 




