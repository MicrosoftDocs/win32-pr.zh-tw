---
description: PublishComponents 動作會從 PublishComponent 資料表管理元件的公告。
ms.assetid: 58d945d7-7dfb-4752-ae19-7e41caca1de7
title: PublishComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c8967e737193922a9dbc3d9e03bc95131d5a63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849158"
---
# <a name="publishcomponents-action"></a><span data-ttu-id="33a50-103">PublishComponents 動作</span><span class="sxs-lookup"><span data-stu-id="33a50-103">PublishComponents Action</span></span>

<span data-ttu-id="33a50-104">PublishComponents 動作會從 [PublishComponent](publishcomponent-table.md) 資料表管理元件的公告。</span><span class="sxs-lookup"><span data-stu-id="33a50-104">The PublishComponents action manages the advertisement of the components from the [PublishComponent](publishcomponent-table.md) table.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="33a50-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="33a50-105">Sequence Restrictions</span></span>

<span data-ttu-id="33a50-106">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="33a50-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="33a50-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="33a50-107">ActionData Messages</span></span>



| <span data-ttu-id="33a50-108">欄位</span><span class="sxs-lookup"><span data-stu-id="33a50-108">Field</span></span> | <span data-ttu-id="33a50-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="33a50-109">Description of action data</span></span>                                   |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="33a50-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="33a50-110">\[1\]</span></span> | <span data-ttu-id="33a50-111">GUID，代表已公告功能的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="33a50-111">GUID representing the component ID of an advertised feature.</span></span> |
| <span data-ttu-id="33a50-112">\[2\]</span><span class="sxs-lookup"><span data-stu-id="33a50-112">\[2\]</span></span> | <span data-ttu-id="33a50-113">元件識別碼的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="33a50-113">Qualifier of component ID.</span></span>                                   |



 

## <a name="remarks"></a><span data-ttu-id="33a50-114">備註</span><span class="sxs-lookup"><span data-stu-id="33a50-114">Remarks</span></span>

<span data-ttu-id="33a50-115">PublishComponents 動作會從 PublishComponents 資料表中，發佈屬於針對公告或安裝所選取之功能的所有元件。</span><span class="sxs-lookup"><span data-stu-id="33a50-115">The PublishComponents action publishes all of the components from the PublishComponents table that belong to features that have been selected for advertisement or installation.</span></span>

 

 



