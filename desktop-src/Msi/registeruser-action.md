---
description: RegisterUser 動作會向安裝程式註冊使用者資訊，以識別產品的使用者。
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692951"
---
# <a name="registeruser-action"></a><span data-ttu-id="c73c6-103">RegisterUser 動作</span><span class="sxs-lookup"><span data-stu-id="c73c6-103">RegisterUser Action</span></span>

<span data-ttu-id="c73c6-104">RegisterUser 動作會向安裝程式註冊使用者資訊，以識別產品的使用者。</span><span class="sxs-lookup"><span data-stu-id="c73c6-104">The RegisterUser action registers the user information with the installer to identify the user of a product.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c73c6-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="c73c6-105">Sequence Restrictions</span></span>

<span data-ttu-id="c73c6-106">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="c73c6-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c73c6-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="c73c6-107">ActionData Messages</span></span>



| <span data-ttu-id="c73c6-108">欄位</span><span class="sxs-lookup"><span data-stu-id="c73c6-108">Field</span></span> | <span data-ttu-id="c73c6-109">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="c73c6-109">Description of action data</span></span>   |
|-------|------------------------------|
| <span data-ttu-id="c73c6-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c73c6-110">\[1\]</span></span> | <span data-ttu-id="c73c6-111">已註冊的使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="c73c6-111">Registered user information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c73c6-112">備註</span><span class="sxs-lookup"><span data-stu-id="c73c6-112">Remarks</span></span>

<span data-ttu-id="c73c6-113">系統管理安裝期間不會執行 RegisterUser 動作。</span><span class="sxs-lookup"><span data-stu-id="c73c6-113">The RegisterUser action is not performed during an administrative installation.</span></span> <span data-ttu-id="c73c6-114">如果 [ValidateProductID 動作](validateproductid-action.md)尚未驗證使用者輸入的產品識別碼，就不會設定 [**ProductID**](productid.md) 屬性，此動作不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="c73c6-114">If the product identifier entered by the user has not been validated by the [ValidateProductID action](validateproductid-action.md), the [**ProductID**](productid.md) property is not set and this action does nothing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c73c6-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c73c6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73c6-116">**使用者**</span><span class="sxs-lookup"><span data-stu-id="c73c6-116">**USERNAME**</span></span>](username.md)
</dt> <dt>

[<span data-ttu-id="c73c6-117">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c73c6-117">**COMPANYNAME**</span></span>](companyname.md)
</dt> <dt>

[<span data-ttu-id="c73c6-118">**產品**</span><span class="sxs-lookup"><span data-stu-id="c73c6-118">**ProductID**</span></span>](productid.md)
</dt> </dl>

 

 



