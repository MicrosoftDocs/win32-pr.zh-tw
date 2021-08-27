---
title: 與 WinEvents 互動
description: 動態注釋執行時間不會傳送 WinEvents;必要時，annotator 會負責傳送適當的事件。 如果您需要傳送 WinEvents，請務必在批註發生之後傳送它們。
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098458"
---
# <a name="interaction-with-winevents"></a>與 WinEvents 互動

動態注釋執行時間不會傳送 [WinEvents](winevents-infrastructure.md);必要時，annotator 會負責傳送適當的事件。 如果您需要傳送 WinEvents，請務必在批註發生之後傳送它們。

例如，如果您使用 [**IAccPropServices：： SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue)來設定專案的 [**Name**](name-property.md)屬性，就會在 **SetPropValue** 傳回之後傳送該物件的 [**事件 \_ 物件 \_ NAMECHANGE**](event-constants.md)事件。

但是，如果您使用 [**IAccPropServices：： SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) 來設定滑杆的 ValueMap，則不需要任何事件，因為設定 ValueMap 不會變更滑杆的值。

 

 




