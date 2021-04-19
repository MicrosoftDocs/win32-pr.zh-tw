---
description: 下表顯示應用程式可用來處理插入號、理由和叢集的各種方法。
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: 使用插入號位置、對齊點和叢集之間的關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973474"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="38589-103">使用插入號位置、對齊點和叢集之間的關聯性</span><span class="sxs-lookup"><span data-stu-id="38589-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="38589-104">下表顯示應用程式可用來處理插入號、理由和叢集的各種方法。</span><span class="sxs-lookup"><span data-stu-id="38589-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="38589-105">Task</span><span class="sxs-lookup"><span data-stu-id="38589-105">Task</span></span>                             | <span data-ttu-id="38589-106">Uniscribe 支援</span><span class="sxs-lookup"><span data-stu-id="38589-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38589-107">依字元叢集的插入號移動</span><span class="sxs-lookup"><span data-stu-id="38589-107">Caret move by character cluster</span></span>  | <span data-ttu-id="38589-108">[**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構之 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** 成員的 *pwLogClust* 參數</span><span class="sxs-lookup"><span data-stu-id="38589-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="38589-109">[**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員</span><span class="sxs-lookup"><span data-stu-id="38589-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="38589-110">字元之間換行</span><span class="sxs-lookup"><span data-stu-id="38589-110">Line breaking between characters</span></span> | <span data-ttu-id="38589-111">[**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構之 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** 成員的 *pwLogClust* 參數</span><span class="sxs-lookup"><span data-stu-id="38589-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="38589-112">[**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員</span><span class="sxs-lookup"><span data-stu-id="38589-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="38589-113">依字組移動插入號</span><span class="sxs-lookup"><span data-stu-id="38589-113">Caret move by word</span></span>               | <span data-ttu-id="38589-114">[**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員</span><span class="sxs-lookup"><span data-stu-id="38589-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="38589-115">單字之間的換行</span><span class="sxs-lookup"><span data-stu-id="38589-115">Line breaking between words</span></span>      | <span data-ttu-id="38589-116">[**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員</span><span class="sxs-lookup"><span data-stu-id="38589-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="38589-117">理由</span><span class="sxs-lookup"><span data-stu-id="38589-117">Justification</span></span>                    | <span data-ttu-id="38589-118">[**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構的 **uJustification** 成員</span><span class="sxs-lookup"><span data-stu-id="38589-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="38589-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="38589-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38589-120">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="38589-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




