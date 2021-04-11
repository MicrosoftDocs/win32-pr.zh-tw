---
description: ISearchJob 介面會定義下列屬性。
ms.assetid: 9e1675e9-fe40-4209-aba9-1cabb4f3ea4c
title: ISearchJob 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c49a5af7435819750451c89ca68f976d76f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113521"
---
# <a name="isearchjob-properties"></a><span data-ttu-id="838c2-103">ISearchJob 屬性</span><span class="sxs-lookup"><span data-stu-id="838c2-103">ISearchJob Properties</span></span>

<span data-ttu-id="838c2-104">[**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="838c2-104">The [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) interface defines the following properties.</span></span>



| <span data-ttu-id="838c2-105">屬性</span><span class="sxs-lookup"><span data-stu-id="838c2-105">Property</span></span>                                      | <span data-ttu-id="838c2-106">描述</span><span class="sxs-lookup"><span data-stu-id="838c2-106">Description</span></span>                                                                                                                                                 |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="838c2-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="838c2-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_asyncstate)   | <span data-ttu-id="838c2-108">取得傳遞至 [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) 方法的呼叫端特定狀態物件。</span><span class="sxs-lookup"><span data-stu-id="838c2-108">Gets the caller-specific state object that is passed to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method.</span></span>                         |
| [<span data-ttu-id="838c2-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="838c2-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_iscompleted) | <span data-ttu-id="838c2-110">取得布林值，指出是否已完整處理 [**IUpdateSearch. BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="838c2-110">Gets a Boolean value that indicates whether the call to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method is completely processed.</span></span> |



 

 

 



