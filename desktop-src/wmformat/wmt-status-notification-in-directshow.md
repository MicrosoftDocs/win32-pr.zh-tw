---
title: WMT_STATUS DirectShow 中的事件通知
description: '\_DirectShow 中的 WMT 狀態事件通知'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media 格式 SDK，WMT_STATUS DirectShow 中的事件通知
- Windows Media Format SDK，事件通知
- Windows Media Format SDK、DirectShow
- " (ASF) 的 Advanced Systems 格式，WMT_STATUS DirectShow 中的事件通知"
- ASF (Advanced Systems Format) ，WMT_STATUS DirectShow 中的事件通知
- Advanced Systems Format (ASF) 、事件通知
- ASF (Advanced Systems Format) ，事件通知
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- DirectShow，事件通知
- DirectShow，WMT_STATUS 事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186016"
---
# <a name="wmt_status-event-notification-in-directshow"></a>\_DirectShow 中的 WMT 狀態事件通知

ASF 讀取器和 ASF 寫入器都會將 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 事件轉送到應用程式。 寫入器會轉送所有這類事件，而且讀取器只會轉送與 DRM 授權取得相關的事件。 若要在您的應用程式中接收這些事件通知，請在事件處理函式中新增 **EC \_ WMT \_ 事件** 的案例。 與事件相關聯的 *lParam1* 參數包含 **WMT \_ 狀態** 代碼 (可 **WMT \_ 錯誤**) ，而 lParam2 包含的 [**AM \_ WMT \_ 事件 \_ 資料**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) 報含 **HRESULT**。

 

 