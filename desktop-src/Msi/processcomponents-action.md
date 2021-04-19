---
description: ProcessComponents 動作會註冊及取消註冊元件、其金鑰路徑和元件用戶端。
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: ProcessComponents 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985289"
---
# <a name="processcomponents-action"></a><span data-ttu-id="1903c-103">ProcessComponents 動作</span><span class="sxs-lookup"><span data-stu-id="1903c-103">ProcessComponents Action</span></span>

<span data-ttu-id="1903c-104">ProcessComponents 動作會註冊及取消註冊元件、其金鑰路徑和元件用戶端。</span><span class="sxs-lookup"><span data-stu-id="1903c-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="1903c-105">ProcessComponents 動作會查詢 [元件資料表](component-table.md) 的 KeyPath 資料行，以判斷 keypaths。</span><span class="sxs-lookup"><span data-stu-id="1903c-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="1903c-106">[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)會使用此註冊來傳回產品用戶端元件的路徑。</span><span class="sxs-lookup"><span data-stu-id="1903c-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1903c-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="1903c-107">Sequence Restrictions</span></span>

<span data-ttu-id="1903c-108">ProcessComponents 動作必須晚于 [InstallInitialize](installinitialize-action.md) 動作。</span><span class="sxs-lookup"><span data-stu-id="1903c-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1903c-109">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="1903c-109">ActionData Messages</span></span>

<span data-ttu-id="1903c-110">針對每個註冊的元件。</span><span class="sxs-lookup"><span data-stu-id="1903c-110">For each component being registered.</span></span>



| <span data-ttu-id="1903c-111">欄位</span><span class="sxs-lookup"><span data-stu-id="1903c-111">Field</span></span> | <span data-ttu-id="1903c-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="1903c-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="1903c-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1903c-113">\[1\]</span></span> | <span data-ttu-id="1903c-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="1903c-114">ProductId</span></span>                       |
| <span data-ttu-id="1903c-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1903c-115">\[2\]</span></span> | <span data-ttu-id="1903c-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="1903c-116">ComponentId</span></span>                     |
| <span data-ttu-id="1903c-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="1903c-117">\[3\]</span></span> | <span data-ttu-id="1903c-118">元件的金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="1903c-118">The key path for the component.</span></span> |



 

<span data-ttu-id="1903c-119">針對正在取消註冊的每個元件。</span><span class="sxs-lookup"><span data-stu-id="1903c-119">For each component being unregistered.</span></span>



| <span data-ttu-id="1903c-120">欄位</span><span class="sxs-lookup"><span data-stu-id="1903c-120">Field</span></span> | <span data-ttu-id="1903c-121">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="1903c-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="1903c-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1903c-122">\[1\]</span></span> | <span data-ttu-id="1903c-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="1903c-123">ProductId</span></span>                  |
| <span data-ttu-id="1903c-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="1903c-124">\[2\]</span></span> | <span data-ttu-id="1903c-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="1903c-125">ComponentId</span></span>                |



 

 

 



