---
title: 資料繫結
description: 資料繫結
ms.assetid: 7fc5f036-8b36-4e0e-a257-173010fe127a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec6b8e66300834939a2b65fddefe947781350b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966271"
---
# <a name="databinding"></a><span data-ttu-id="e6ff6-103">資料繫結</span><span class="sxs-lookup"><span data-stu-id="e6ff6-103">Databinding</span></span>

<span data-ttu-id="e6ff6-104">已加入新的資料系結屬性，只有當焦點離開控制項或在所有屬性變更通知期間，才會讓屬性區分通訊的變更。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-104">A new databinding attribute has been added to allow properties distinguish between communicating changes only when focus leaves the control or during all property change notifications.</span></span>

<span data-ttu-id="e6ff6-105">新的屬性（稱為 ImmediateBind）可讓控制項區分兩種不同類型的可系結屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-105">The new attribute, known as ImmediateBind, enables controls to differentiate two different types of bindable properties.</span></span> <span data-ttu-id="e6ff6-106">其中一種可系結屬性必須通知資料庫的每項變更，例如，有一個核取方塊控制項，也就是每個變更都需要傳送到基礎資料庫，即使控制項尚未遺失焦點也一樣。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-106">One type of bindable property needs to notify every change to the database, for example with a check box control where every change needs to be sent through to the underlying database even though the control has not lost the focus.</span></span> <span data-ttu-id="e6ff6-107">不過，例如 listbox 的控制項只會希望在控制項失去焦點時，將屬性的變更通知給資料庫，因為使用者可能會在尋找所要的設定之後，使用方向鍵來變更反白顯示的選取專案，讓變更通知在每次使用者按下方向鍵時，將變更通知傳送至資料庫，以提供無法接受的效能。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-107">However controls such as a listbox only wish to have the change of a property notified to the database when the control loses focus, as the user may have changed the highlighted selection with the arrow keys before finding the desired setting, to have the change notification sent to the database every time that the user hit the arrow key would be give unacceptable performance.</span></span> <span data-ttu-id="e6ff6-108">新的 [立即系結] 屬性可讓表單上的個別可系結屬性指定此行為，當設定此位時，將會通知所有變更。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-108">The new immediate bind property allows individual bindable properties on a form to have this behavior specified, when this bit is set all changes will be notified.</span></span>

<span data-ttu-id="e6ff6-109">新的 ImmediateBind 位會對應至新的 VARFLAG \_ FIMMEDIATEBIND (0x80) 和 FUNCFLAG \_ FIMMEDIATEBIND (0x80) 位在 VARFLAGS 介面的 FUNCFLAGS 和 ITypeInfo 列舉中[](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) ，以便檢查屬性屬性。</span><span class="sxs-lookup"><span data-stu-id="e6ff6-109">The new ImmediateBind bit maps through to the new VARFLAG\_FIMMEDIATEBIND (0x80) and the FUNCFLAG\_FIMMEDIATEBIND (0x80) bits in the VARFLAGS and FUNCFLAGS enumerations for the [ITypeInfo](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interface allowing for the properties attributes to be inspected.</span></span>

 

 