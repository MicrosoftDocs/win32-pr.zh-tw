---
title: 處理註冊
description: HTTP 伺服器 Api 會在註冊期間使用路由資料庫來套用存取檢查。
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1e02d2511d9967454d5cbddd93b2c0380d1172
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463901"
---
# <a name="processing-registrations"></a><span data-ttu-id="54d92-103">處理註冊</span><span class="sxs-lookup"><span data-stu-id="54d92-103">Processing Registrations</span></span>

<span data-ttu-id="54d92-104">HTTP 伺服器 Api 會在註冊期間使用路由資料庫來套用存取檢查。</span><span class="sxs-lookup"><span data-stu-id="54d92-104">The HTTP Server APIs use the routing database to apply access checks during registrations.</span></span> <span data-ttu-id="54d92-105">[UrlPrefix](urlprefix-strings.md)的註冊必須通過一系列的存取檢查，以確保註冊命名空間的使用者有存取權限。</span><span class="sxs-lookup"><span data-stu-id="54d92-105">A registration for a [UrlPrefix](urlprefix-strings.md) must pass a series of access checks to ensure that the user registering for the namespace has access rights.</span></span> <span data-ttu-id="54d92-106">使用 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函數來新增註冊。</span><span class="sxs-lookup"><span data-stu-id="54d92-106">Use the [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) function to add a new registration.</span></span>

<span data-ttu-id="54d92-107">**使用 HttpAddUrl 新增註冊**</span><span class="sxs-lookup"><span data-stu-id="54d92-107">**To add a new registration with HttpAddUrl**</span></span>

1.  <span data-ttu-id="54d92-108">如果 UrlPrefix 中的埠號碼具有與 UrlPrefix 中配置不同的配置保留或註冊，則註冊會失敗。</span><span class="sxs-lookup"><span data-stu-id="54d92-108">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="54d92-109">在相同的埠上無法支援 HTTP 和 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="54d92-109">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="54d92-110">註冊時，會將註冊帶到適當的 bucket。</span><span class="sxs-lookup"><span data-stu-id="54d92-110">The registration is slotted into the appropriate bucket for the registration.</span></span> <span data-ttu-id="54d92-111">值區是以 URL 的主機類型為基礎，如 [路由傳入要求](routing-incoming-requests.md) 一節中所述。</span><span class="sxs-lookup"><span data-stu-id="54d92-111">The buckets are based on the host type of the URL as outlined in the [Routing Incoming Requests](routing-incoming-requests.md) section.</span></span> <span data-ttu-id="54d92-112">以下是相對於這個特定值區的步驟。</span><span class="sxs-lookup"><span data-stu-id="54d92-112">The following steps are relative to this particular bucket.</span></span>
3.  <span data-ttu-id="54d92-113">如果存在重複的註冊專案，則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="54d92-113">If a duplicate registration entry exists, return an error code.</span></span>
4.  <span data-ttu-id="54d92-114">選取具有與 UrlPrefix 相同的配置、主機和埠元件的保留專案。</span><span class="sxs-lookup"><span data-stu-id="54d92-114">Select reservation entries with scheme, host and port components that are equal to those of the UrlPrefix.</span></span> <span data-ttu-id="54d92-115">從這些專案找出具有最長 **relativeUri** 相符專案的專案。</span><span class="sxs-lookup"><span data-stu-id="54d92-115">From these, locate the entry with the longest **relativeUri** match.</span></span> <span data-ttu-id="54d92-116">如果專案存在，請根據與該專案相關聯的 ACL 來檢查許可權，並傳回成功。</span><span class="sxs-lookup"><span data-stu-id="54d92-116">If the entry exists, check permissions based on the ACL associated with that entry and return success.</span></span> <span data-ttu-id="54d92-117">如果專案不存在，則傳回已存在的錯誤程式 \_ \_ 代碼。</span><span class="sxs-lookup"><span data-stu-id="54d92-117">If the entry does not exist, return an ERROR\_ALREADY\_EXISTS code.</span></span>

<span data-ttu-id="54d92-118">下列範例說明在路由資料庫中安裝註冊的程式。</span><span class="sxs-lookup"><span data-stu-id="54d92-118">The following examples illustrate the process to install a registration in the routing database.</span></span> <span data-ttu-id="54d92-119">保留1和2存在於路由資料庫中。</span><span class="sxs-lookup"><span data-stu-id="54d92-119">Reservations 1 and 2 exist in the routing database.</span></span>

-   <span data-ttu-id="54d92-120">保留1： `https://+:80/vroot/subdir/` 適用于使用者 A 和使用者 C。此保留專案會放在 "+" bucket 中。</span><span class="sxs-lookup"><span data-stu-id="54d92-120">Reservation 1: `https://+:80/vroot/subdir/` for User A and User C. This reservation is placed in the "+" bucket.</span></span>
-   <span data-ttu-id="54d92-121">保留2： `https://adatum.com:80/vroot/` 適用于使用者 B。此保留專案會放在「明確主機」 bucket 中。</span><span class="sxs-lookup"><span data-stu-id="54d92-121">Reservation 2: `https://adatum.com:80/vroot/` for User B. This reservation is placed in the "Explicit Host" bucket.</span></span>
-   <span data-ttu-id="54d92-122">註冊： `https://+:80/vroot/subdir/` 依使用者 B 而失敗，因為保留1。</span><span class="sxs-lookup"><span data-stu-id="54d92-122">Registration: `https://+:80/vroot/subdir/` by User B fails due to reservation 1.</span></span>
-   <span data-ttu-id="54d92-123">註冊： `https://adatum.com:80/vroot/subdir/` 使用者 B 由於保留2而成功。</span><span class="sxs-lookup"><span data-stu-id="54d92-123">Registration: `https://adatum.com:80/vroot/subdir/` by User B succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="54d92-124">註冊： `https://adatum.com:80/vroot/subdir/` 依使用者 C 失敗，因為有更明確的保留2。</span><span class="sxs-lookup"><span data-stu-id="54d92-124">Registration: `https://adatum.com:80/vroot/subdir/` by User C fails due to the more explicit reservation 2.</span></span> <span data-ttu-id="54d92-125">強式萬用字元保留在明確保留或註冊的內容中沒有意義。</span><span class="sxs-lookup"><span data-stu-id="54d92-125">The strong wildcard reservation does not have meaning within the context of the explicit reservation or registration.</span></span>
-   <span data-ttu-id="54d92-126">註冊： `https://+:80/vroot/subdir/` 使用者 A 成功，因為保留1。</span><span class="sxs-lookup"><span data-stu-id="54d92-126">Registration: `https://+:80/vroot/subdir/` by User A succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="54d92-127">註冊： `https://adatum.com:80/vroot/anotherdir/` 使用者 B 由於保留2而成功。</span><span class="sxs-lookup"><span data-stu-id="54d92-127">Registration: `https://adatum.com:80/vroot/anotherdir/` by User B succeeds due to reservation 2.</span></span>

<span data-ttu-id="54d92-128">註冊的存取檢查不包含委派許可權的檢查。</span><span class="sxs-lookup"><span data-stu-id="54d92-128">The access check for registration does not include checks for delegation privileges.</span></span> <span data-ttu-id="54d92-129">不會根據保留來檢查存取 (請參閱 [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)) 。</span><span class="sxs-lookup"><span data-stu-id="54d92-129">There are no access checks based on reservations (see [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)).</span></span> <span data-ttu-id="54d92-130">刪除註冊的唯一需求，就是呼叫進程必須建立註冊。</span><span class="sxs-lookup"><span data-stu-id="54d92-130">The only requirement for deleting a registration us that the calling process must have created the registration.</span></span>

 

 




