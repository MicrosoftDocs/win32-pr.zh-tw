---
title: 與 WinEvents 互動
description: 動態注釋執行時間不會傳送 WinEvents;必要時，annotator 會負責傳送適當的事件。 如果您需要傳送 WinEvents，請務必在批註發生之後傳送它們。
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "106965001"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="67566-104">與 WinEvents 互動</span><span class="sxs-lookup"><span data-stu-id="67566-104">Interaction with WinEvents</span></span>

<span data-ttu-id="67566-105">動態注釋執行時間不會傳送 [WinEvents](winevents-infrastructure.md);必要時，annotator 會負責傳送適當的事件。</span><span class="sxs-lookup"><span data-stu-id="67566-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="67566-106">如果您需要傳送 WinEvents，請務必在批註發生之後傳送它們。</span><span class="sxs-lookup"><span data-stu-id="67566-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="67566-107">例如，如果您使用 [**IAccPropServices：： SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue)來設定專案的 [**Name**](name-property.md)屬性，就會在 **SetPropValue** 傳回之後傳送該物件的 [**事件 \_ 物件 \_ NAMECHANGE**](event-constants.md)事件。</span><span class="sxs-lookup"><span data-stu-id="67566-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="67566-108">但是，如果您使用 [**IAccPropServices：： SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) 來設定滑杆的 ValueMap，則不需要任何事件，因為設定 ValueMap 不會變更滑杆的值。</span><span class="sxs-lookup"><span data-stu-id="67566-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




