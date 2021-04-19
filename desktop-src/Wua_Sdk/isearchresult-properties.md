---
description: ISearchResult 介面會定義下列屬性。
ms.assetid: 12237d7b-edb1-45b1-b4e1-a85261ee18ce
title: ISearchResult 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2e8e77a4533d7fcac2a34bb3b6fd1c4b74b77b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972653"
---
# <a name="isearchresult-properties"></a><span data-ttu-id="b0574-103">ISearchResult 屬性</span><span class="sxs-lookup"><span data-stu-id="b0574-103">ISearchResult Properties</span></span>

<span data-ttu-id="b0574-104">[**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="b0574-104">The [**ISearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult) interface defines the following properties.</span></span>



| <span data-ttu-id="b0574-105">屬性</span><span class="sxs-lookup"><span data-stu-id="b0574-105">Property</span></span>                                               | <span data-ttu-id="b0574-106">描述</span><span class="sxs-lookup"><span data-stu-id="b0574-106">Description</span></span>                                                                                                   |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0574-107">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="b0574-107">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchresult-get_resultcode)         | <span data-ttu-id="b0574-108">取得指定搜尋結果的 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 列舉。</span><span class="sxs-lookup"><span data-stu-id="b0574-108">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) enumeration that specifies the result of a search.</span></span> |
| [<span data-ttu-id="b0574-109">**RootCategories**</span><span class="sxs-lookup"><span data-stu-id="b0574-109">**RootCategories**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchresult-get_rootcategories) | <span data-ttu-id="b0574-110">取得電腦上目前可用之根類別的介面集合。</span><span class="sxs-lookup"><span data-stu-id="b0574-110">Gets an interface collection of the root categories that are currently available on the computer.</span></span>             |
| [<span data-ttu-id="b0574-111">**更新**</span><span class="sxs-lookup"><span data-stu-id="b0574-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchresult-get_updates)               | <span data-ttu-id="b0574-112">取得搜尋所產生之更新的介面集合。</span><span class="sxs-lookup"><span data-stu-id="b0574-112">Gets an interface collection of the updates that result from a search.</span></span>                                        |
| [<span data-ttu-id="b0574-113">**警告**</span><span class="sxs-lookup"><span data-stu-id="b0574-113">**Warnings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchresult-get_warnings)             | <span data-ttu-id="b0574-114">取得搜尋所產生的警告集合。</span><span class="sxs-lookup"><span data-stu-id="b0574-114">Gets a collection of the warnings that result from a search.</span></span>                                                  |



 

 

 



