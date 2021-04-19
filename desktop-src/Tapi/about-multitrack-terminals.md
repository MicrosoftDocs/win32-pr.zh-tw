---
description: Multitrack 終端機可視為是其他終端機集合的終端機。 每個子終端機 (&\# 0034; 追蹤&\# 0034; ) 可以是 multitrack 終端機或單一追蹤終端機。
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: 關於 Multitrack 終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998106"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="7ec8f-104">關於 Multitrack 終端機</span><span class="sxs-lookup"><span data-stu-id="7ec8f-104">About Multitrack Terminals</span></span>

<span data-ttu-id="7ec8f-105">Multitrack 終端機可視為是其他終端機集合的終端機。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="7ec8f-106">每個子終端 (「追蹤」 ) 可以是 multitrack 終端機或單一追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="7ec8f-107">所有 multitrack 的終端機都會公開 [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) 介面，其中包括列舉、建立和移除 multitrack 終端機追蹤終端機的一般方法。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="7ec8f-108">所有的終端機、單一追蹤和 multitrack 都會公開 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="7ec8f-109">具有 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面指標的用戶端可以藉由查詢 [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) 介面的終端機，來探索終端機是否為 multitrack 或單一追蹤，此介面只會在 multitrack 端子上公開。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="7ec8f-110">父終端機會使用其追蹤終端機的 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面，或可能需要追蹤終端機才能公開私用介面。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="7ec8f-111">如需詳細資訊，請參閱 [追蹤終端](track-terminals.md)機。</span><span class="sxs-lookup"><span data-stu-id="7ec8f-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
