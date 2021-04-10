---
title: 執行緒管理員
description: 執行緒管理員是 TSF 管理員的基礎元件。
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- '執行緒管理員文字服務架構 (TSF) '
- TSF (文字服務架構) ，執行緒管理員
- 文字服務，執行緒管理員
- 具有 TSF 功能的應用程式，執行緒管理員
- 執行緒管理員
- TSF 管理員
- 事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023723"
---
# <a name="thread-manager"></a>執行緒管理員

執行緒管理員是 TSF 管理員的基礎元件。 執行緒管理員會執行與應用程式和文字服務 (用戶端) 相關的一般工作。 這些工作包括（但不限於）啟用和停用 TSF 文字服務、建立檔管理員，以及維護檔和輸入焦點之間的適當關聯性。 執行緒管理員是由 [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) 介面所定義。

TSF 管理員提供的大部分介面和物件都可以使用執行緒管理員介面提供的方法來取得。

## <a name="applications"></a>應用程式

應用程式會使用 CLSID TFThreadMgr 呼叫 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來建立執行緒管理員物件 \_ 。

## <a name="text-services"></a>文字服務

文字服務會取得 text service [ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) 方法中的執行緒管理員物件。

## <a name="event-notifications"></a>事件通知

執行緒管理員也會提供事件通知給用戶端。 在 TSF 中，事件通知是透過事件接收器（COM 物件）來提供。 為了接收來自執行緒管理員的通知，用戶端會執行 [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) 物件並安裝事件接收器。 藉由查詢 ITfSource 的執行緒管理員 \_ ，並使用 iid ITfThreadMgrEventSink 呼叫 [ITfSource：： AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) ，即可安裝事件接收器 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor：： Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 