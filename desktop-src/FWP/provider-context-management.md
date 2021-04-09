---
title: 提供者內容管理
description: 提供者內容管理
ms.assetid: A73A6171-C81B-48EF-A689-3219E0B6B7C3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7970cdd6f3a69760a74ba4f0419ecb5022a339
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682000"
---
# <a name="provider-context-management"></a><span data-ttu-id="450e6-103">提供者內容管理</span><span class="sxs-lookup"><span data-stu-id="450e6-103">Provider Context Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="450e6-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="450e6-104">In this section</span></span>

-   [<span data-ttu-id="450e6-105">**FWPM \_ 提供者 \_ 內容 \_ 變更 \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="450e6-105">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   [<span data-ttu-id="450e6-106">**FwpmProviderCoNtextAdd0**</span><span class="sxs-lookup"><span data-stu-id="450e6-106">**FwpmProviderContextAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)
-   [<span data-ttu-id="450e6-107">**FwpmProviderCoNtextAdd1**</span><span class="sxs-lookup"><span data-stu-id="450e6-107">**FwpmProviderContextAdd1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1)
-   [<span data-ttu-id="450e6-108">**FwpmProviderCoNtextAdd2**</span><span class="sxs-lookup"><span data-stu-id="450e6-108">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="450e6-109">**FwpmProviderCoNtextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="450e6-109">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="450e6-110">**FwpmProviderCoNtextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="450e6-110">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="450e6-111">**FwpmProviderCoNtextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="450e6-111">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="450e6-112">**FwpmProviderCoNtextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="450e6-112">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   [<span data-ttu-id="450e6-113">**FwpmProviderCoNtextEnum0**</span><span class="sxs-lookup"><span data-stu-id="450e6-113">**FwpmProviderContextEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0)
-   [<span data-ttu-id="450e6-114">**FwpmProviderCoNtextEnum1**</span><span class="sxs-lookup"><span data-stu-id="450e6-114">**FwpmProviderContextEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1)
-   [<span data-ttu-id="450e6-115">**FwpmProviderCoNtextEnum2**</span><span class="sxs-lookup"><span data-stu-id="450e6-115">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="450e6-116">**FwpmProviderCoNtextGetById0**</span><span class="sxs-lookup"><span data-stu-id="450e6-116">**FwpmProviderContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0)
-   [<span data-ttu-id="450e6-117">**FwpmProviderCoNtextGetById1**</span><span class="sxs-lookup"><span data-stu-id="450e6-117">**FwpmProviderContextGetById1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1)
-   [<span data-ttu-id="450e6-118">**FwpmProviderCoNtextGetById2**</span><span class="sxs-lookup"><span data-stu-id="450e6-118">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="450e6-119">**FwpmProviderCoNtextGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="450e6-119">**FwpmProviderContextGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0)
-   [<span data-ttu-id="450e6-120">**FwpmProviderCoNtextGetByKey1**</span><span class="sxs-lookup"><span data-stu-id="450e6-120">**FwpmProviderContextGetByKey1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1)
-   [<span data-ttu-id="450e6-121">**FwpmProviderCoNtextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="450e6-121">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="450e6-122">**FwpmProviderCoNtextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="450e6-122">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="450e6-123">**FwpmProviderCoNtextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="450e6-123">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="450e6-124">**FwpmProviderCoNtextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="450e6-124">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="450e6-125">**FwpmProviderCoNtextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="450e6-125">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="450e6-126">**FwpmProviderCoNtextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="450e6-126">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

 

 