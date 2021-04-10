---
title: Windows 事件記錄檔
description: Windows 事件記錄檔 API 會定義您用來撰寫檢測資訊清單的架構。
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842707"
---
# <a name="windows-event-log"></a>Windows 事件記錄檔

## <a name="purpose"></a>目的

Windows 事件記錄檔 API 會定義您用來撰寫檢測資訊清單的架構。 檢測資訊清單會識別您的事件提供者和其所記錄的事件。 此 API 也包含事件取用者（例如 [事件檢視器](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))）將用來讀取和轉譯事件的函式。 若要寫入資訊清單中定義的事件，請使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) API 中包含的函式。

Windows 事件記錄檔會取代從 Windows Vista 作業系統開始的 [事件記錄](/windows/desktop/EventLog/event-logging) API。

## <a name="developer-audience"></a>開發人員對象

Windows 事件記錄檔是針對 C/c + + 程式設計人員所設計。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 和 Windows Server 2008 開始，windows 事件記錄檔已包含在作業系統中。

如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。

如需完整的版本歷程記錄，請參閱 [新功能](what-s-new.md)。

## <a name="in-this-section"></a>本節內容


| 主題                                                        | 描述                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [使用 Windows 事件記錄檔](using-windows-event-log.md)        | 說明如何使用 Windows 事件記錄檔 API 的程式指南。                                 |
| [Windows 事件記錄檔參考](windows-event-log-reference.md)| API 包含的資料類型、函數、列舉、結構、常數和架構。|