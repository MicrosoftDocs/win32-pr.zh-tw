---
title: 授權外掛程式方法
description: 所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。 某些回呼機制會呼叫多次，直到報告所有結果為止。
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965982"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="16459-104">授權外掛程式方法</span><span class="sxs-lookup"><span data-stu-id="16459-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="16459-105">所有授權外掛程式進入點都有回呼機制，可報告呼叫成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="16459-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="16459-106">某些回呼機制會呼叫多次，直到報告所有結果為止。</span><span class="sxs-lookup"><span data-stu-id="16459-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="16459-107">下表提供授權回呼方法的總覽。</span><span class="sxs-lookup"><span data-stu-id="16459-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="16459-108">方法</span><span class="sxs-lookup"><span data-stu-id="16459-108">Method</span></span>                                                                           | <span data-ttu-id="16459-109">描述</span><span class="sxs-lookup"><span data-stu-id="16459-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="16459-110">**WSManPluginAuthzOperationComplete**</span><span class="sxs-lookup"><span data-stu-id="16459-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="16459-111">報告成功或失敗的使用者操作。</span><span class="sxs-lookup"><span data-stu-id="16459-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="16459-112">**WSManPluginAuthzQueryQuotaComplete**</span><span class="sxs-lookup"><span data-stu-id="16459-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="16459-113">報告與指定使用者相關的配額詳細資料。</span><span class="sxs-lookup"><span data-stu-id="16459-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="16459-114">**WSManPluginAuthzUserComplete**</span><span class="sxs-lookup"><span data-stu-id="16459-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="16459-115">報告成功或失敗的使用者連接授權。</span><span class="sxs-lookup"><span data-stu-id="16459-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




