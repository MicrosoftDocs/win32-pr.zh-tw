---
description: PublishProduct 動作會使用系統來管理產品資訊的公告。 如果產品處於公告模式或正在安裝或重新安裝任何功能，則此動作會發佈產品。
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: PublishProduct 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996719"
---
# <a name="publishproduct-action"></a><span data-ttu-id="22693-104">PublishProduct 動作</span><span class="sxs-lookup"><span data-stu-id="22693-104">PublishProduct Action</span></span>

<span data-ttu-id="22693-105">PublishProduct 動作會使用系統來管理產品資訊的公告。</span><span class="sxs-lookup"><span data-stu-id="22693-105">The PublishProduct action manages the advertisement of the product information with the system.</span></span> <span data-ttu-id="22693-106">如果產品處於公告模式或正在安裝或重新安裝任何功能，則此動作會發佈產品。</span><span class="sxs-lookup"><span data-stu-id="22693-106">This action publishes the product if the product is in advertise mode or if any feature is being installed or reinstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="22693-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="22693-107">Sequence Restrictions</span></span>

<span data-ttu-id="22693-108">PublishProduct 動作必須晚于 [PublishFeatures](publishfeatures-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="22693-108">The PublishProduct action must come after the [PublishFeatures](publishfeatures-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="22693-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="22693-109">ActionData Messages</span></span>



| <span data-ttu-id="22693-110">欄位</span><span class="sxs-lookup"><span data-stu-id="22693-110">Field</span></span> | <span data-ttu-id="22693-111">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="22693-111">Description of Action Data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="22693-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="22693-112">\[1\]</span></span> | <span data-ttu-id="22693-113">已公告產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="22693-113">Identifier of advertised product.</span></span> |



 

 

 



