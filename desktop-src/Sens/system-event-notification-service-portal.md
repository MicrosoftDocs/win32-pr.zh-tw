---
description: 從在行動電腦上執行的程式監視系統事件通知，以判斷網路連接頻寬和延遲。 撰寫適用于行動計算和高延遲 Lan 的優化應用程式。
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: 系統事件通知服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944943"
---
# <a name="system-event-notification-service"></a>系統事件通知服務

## <a name="purpose"></a>目的

專為行動使用者所設計的應用程式需要一組獨特的連接功能和通知。 在過去，這些個別的應用程式必須在內部執行這些功能。 系統事件通知服務 (SENS) 現在會在作業系統中提供這些功能，為應用程式建立統一的連線和通知介面。 使用 SENS 開發人員可以從應用程式內判斷連接頻寬和延遲資訊，並根據這些條件將應用程式的作業優化。

## <a name="where-applicable"></a>適用時

SENS 的連線能力和通知適用于為行動電腦或連接到高延遲區域網路的電腦所撰寫的應用程式。

## <a name="developer-audience"></a>開發人員對象

本檔適用于開發行動電腦運算和高延遲區域網路應用程式的軟體發展人員。 本檔提供系統事件通知服務的所有部分的完整參考，包括 SENS 物件和支援的方法。

## <a name="run-time-requirements"></a>執行階段需求求

需要 Microsoft Windows XP 或更新版本。 如需哪些作業系統需要哪些作業系統才能使用特定介面或功能的相關資訊，請參閱檔的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                                              | 描述                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [概觀](about-system-event-notification-service.md)<br/> | 關於系統事件通知服務的一般資訊。<br/>               |
| [參考](sens-reference.md)<br/>                         | 系統事件通知服務方法和介面的檔。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IEventSubscription**](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
