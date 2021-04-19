---
description: 使用 lineSetTerminal 函式，應用程式可以控制或隱藏指定的低層級事件的路由， (在切換和站) 之間交換至裝置。
ms.assetid: 36658d83-0ea4-4f62-b2e5-c0f6d6569d0d
title: 事件路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6749969faf89ac0212c19049fe02c9dad57a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986352"
---
# <a name="event-routing"></a>事件路由

使用 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) 函式，應用程式可以控制或隱藏指定的低層級事件的路由， (在切換和站) 之間交換至裝置。 使用 **lineSetTerminal**，應用程式會指定這些事件 (的終端機裝置，例如行、位址或) 路由傳送的呼叫媒體串流事件。

不同事件類別的路由可以個別控制，允許針對每個事件類別指定個別的終端機。 事件類別包括燈、按鈕、顯示、響鈴、hookswitch 和媒體串流。

例如，如果服務提供者和硬體能夠這樣做，則呼叫 (聲音的媒體串流（例如) ）可以傳送至任何感應器裝置。 一般情況下， *感應器* 的意思與 TAPI 中的 *hookswitch* 裝置（具有麥克風和喇叭的東西）相同。 從切換至電話的響鈴事件可以對應到電腦畫面上的視覺效果警示，也可以將它們路由傳送至電話裝置。 您可以忽略燈泡事件和顯示事件，或將其路由傳送至電話裝置， (看起來會像一般的電話設定) 。 最後，在手機裝置上按下按鈕時，可能會或不會傳遞至該行。 在任何情況下，這一行的低層級信號路由並不會影響 TAPI 行部分的操作，這一律會將低層級的事件對應至正常運作的功能對等專案。 若要判斷終端機線路裝置可用 (及其功能) ，請參閱線路裝置的功能與 [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)。

假設應用程式一開始會抑制使用 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal))  (所有事件的路由，且使用者選取耳機作為目前的 i/o 裝置。 傳入的呼叫會傳送 [**一行 \_ CALLSTATE**](line-callstate.md)訊息，以及含有 *響鈴* 指示的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md)訊息。 由於會抑制所有事件的路由，因此環形事件不會路由傳送至電話，因此會抑制響鈴。 相反地，應用程式會以快顯對話方塊通知使用者，並在耳機中發出系統嗶聲。

使用者決定接聽通話。 由於使用者目前的 i/o 裝置是耳機，因此電話語音應用程式會叫用傳入電話上的 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ，將通話的媒體路由傳送到耳機並接聽通話。 應用程式也可能會叫用 **lineSetTerminal** 來路由燈，並將資訊事件顯示在電話組中，如此一來，它就會正常運作。

第二個範例是假設來電是在使用者的電腦上發出警示。 使用者不需要使用滑鼠來選取答案選項，而是決定只挑選手機的話筒來接聽通話。 電話上的 offhook 狀態會將訊息傳送至應用程式。 應用程式可以將此狀態解釋為使用者要求，以選取電話聽筒來進行交談。 然後，應用程式會叫用 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ，將通話的語音資料路由傳送至電話組。

 

 



