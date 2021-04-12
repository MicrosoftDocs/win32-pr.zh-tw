---
title: 具有對應 WinEvents 的注釋屬性
description: 覆寫經常變更的屬性時請務必小心，特別是在 New-winevent (（例如狀態、值、和某些控制項）所檢查的屬性，) 的名稱屬性。
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375812"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="37269-103">具有對應 WinEvents 的注釋屬性</span><span class="sxs-lookup"><span data-stu-id="37269-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="37269-104">覆寫經常變更的屬性時請務必小心，特別是在 New-winevent (（例如 [**狀態**](state-property.md)、 [**值**](value-property.md)、和某些控制項）所檢查的屬性，) 的 [**名稱**](name-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="37269-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="37269-105">在許多情況下（特別是針對使用者和 ComCtl 控制項），New-winevent 會在控制項的擁有者收到通知之前，傳送控制項的擁有者， (通常透過 [WM \_ 通知](../controls/wm-notify.md)) 。</span><span class="sxs-lookup"><span data-stu-id="37269-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="37269-106">在 WM 通知處理常式中使用 [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) 更新屬性 \_ 會太晚; 使用內容內部攔截的用戶端已存取舊的值。</span><span class="sxs-lookup"><span data-stu-id="37269-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="37269-107">您可以使用 [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver))  (的回呼伺服器物件來處理這些類型的屬性;但是，伺服器無法使用在 WM 通知處理常式中更新的任何狀態， \_ 因為尚未呼叫該處理常式。</span><span class="sxs-lookup"><span data-stu-id="37269-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="37269-108">例如，不使用在 WM 通知處理常式中更新且即將過期的快取目前值變數， \_ [**IAccPropServer：： GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) 回呼物件應該會直接將訊息傳送至控制項，以取得其真正的目前值以產生必要的屬性。</span><span class="sxs-lookup"><span data-stu-id="37269-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 