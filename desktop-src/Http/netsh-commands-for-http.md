---
title: 適用于 HTTP 的 Netsh 命令
description: 您可以使用適用于 HTTP 內容的 Netsh 命令來查詢和設定 HTTP.sys 設定和參數。
ms.assetid: 695c309c-ab43-4c6a-b5f6-5bb9f715bf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f6e0fdd0813284e36d2fb9fb826929c67df63c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674556"
---
# <a name="netsh-commands-for-http"></a><span data-ttu-id="41a7c-103">適用于 HTTP 的 Netsh 命令</span><span class="sxs-lookup"><span data-stu-id="41a7c-103">Netsh commands for HTTP</span></span>

<span data-ttu-id="41a7c-104">您可以使用適用于 HTTP 內容的 Netsh 命令來查詢和設定 HTTP.sys 設定和參數。</span><span class="sxs-lookup"><span data-stu-id="41a7c-104">You can use the Netsh commands for HTTP context to query and configure HTTP.sys settings and parameters.</span></span>

<span data-ttu-id="41a7c-105">您可以在 Windows Vista 作業系統的命令提示字元中，或在 **netsh HTTP** 內容的命令提示字元中執行這些命令。</span><span class="sxs-lookup"><span data-stu-id="41a7c-105">You can run these commands at the command prompt in the Windows Vista operating system or at the command prompt for the **netsh http** context.</span></span> <span data-ttu-id="41a7c-106">若要在 Windows Vista 的命令提示字元中使用這些命令，您必須輸入 **netsh HTTP** ，然後輸入命令和參數，如下列語法所示。</span><span class="sxs-lookup"><span data-stu-id="41a7c-106">For these commands to work at the command prompt in Windows Vista, you must type **netsh http** before typing commands and parameters as they appear in the syntax below.</span></span> <span data-ttu-id="41a7c-107">若要在命令提示字元中查看命令的說明，請輸入 \* CommandName \***/？**，其中 *CommandName* 是命令的名稱。</span><span class="sxs-lookup"><span data-stu-id="41a7c-107">To view help for a command at the command prompt, type \*CommandName\***/?**, where *CommandName* is the name of the command.</span></span>

<span data-ttu-id="41a7c-108">若要查看命令語法，請參閱下列命令：</span><span class="sxs-lookup"><span data-stu-id="41a7c-108">To view the command syntax, see the commands:</span></span>

-   [<span data-ttu-id="41a7c-109">**add iplisten**</span><span class="sxs-lookup"><span data-stu-id="41a7c-109">**add iplisten**</span></span>](add-iplisten.md)
-   [<span data-ttu-id="41a7c-110">**add sslcert**</span><span class="sxs-lookup"><span data-stu-id="41a7c-110">**add sslcert**</span></span>](add-sslcert.md)
-   [<span data-ttu-id="41a7c-111">**add timeout**</span><span class="sxs-lookup"><span data-stu-id="41a7c-111">**add timeout**</span></span>](add-timeout.md)
-   [<span data-ttu-id="41a7c-112">**add urlacl**</span><span class="sxs-lookup"><span data-stu-id="41a7c-112">**add urlacl**</span></span>](add-urlacl.md)
-   [<span data-ttu-id="41a7c-113">**delete cache**</span><span class="sxs-lookup"><span data-stu-id="41a7c-113">**delete cache**</span></span>](delete-cache.md)
-   [<span data-ttu-id="41a7c-114">**delete iplisten**</span><span class="sxs-lookup"><span data-stu-id="41a7c-114">**delete iplisten**</span></span>](delete-iplisten.md)
-   [<span data-ttu-id="41a7c-115">**delete sslcert**</span><span class="sxs-lookup"><span data-stu-id="41a7c-115">**delete sslcert**</span></span>](delete-sslcert.md)
-   [<span data-ttu-id="41a7c-116">**delete timeout**</span><span class="sxs-lookup"><span data-stu-id="41a7c-116">**delete timeout**</span></span>](delete-timeout.md)
-   [<span data-ttu-id="41a7c-117">**delete urlacl**</span><span class="sxs-lookup"><span data-stu-id="41a7c-117">**delete urlacl**</span></span>](delete-urlacl.md)
-   [<span data-ttu-id="41a7c-118">**flush logbuffer**</span><span class="sxs-lookup"><span data-stu-id="41a7c-118">**flush logbuffer**</span></span>](flush-logbuffer.md)
-   [<span data-ttu-id="41a7c-119">**show cachestate**</span><span class="sxs-lookup"><span data-stu-id="41a7c-119">**show cachestate**</span></span>](show-cachestate.md)
-   [<span data-ttu-id="41a7c-120">**show iplisten**</span><span class="sxs-lookup"><span data-stu-id="41a7c-120">**show iplisten**</span></span>](show-iplisten.md)
-   [<span data-ttu-id="41a7c-121">**show servicestate**</span><span class="sxs-lookup"><span data-stu-id="41a7c-121">**show servicestate**</span></span>](show-servicestate.md)
-   [<span data-ttu-id="41a7c-122">**show sslcert**</span><span class="sxs-lookup"><span data-stu-id="41a7c-122">**show sslcert**</span></span>](show-sslcert.md)
-   [<span data-ttu-id="41a7c-123">**show timeout**</span><span class="sxs-lookup"><span data-stu-id="41a7c-123">**show timeout**</span></span>](show-timeout.md)
-   [<span data-ttu-id="41a7c-124">**show urlacl**</span><span class="sxs-lookup"><span data-stu-id="41a7c-124">**show urlacl**</span></span>](show-urlacl.md)

 

 




