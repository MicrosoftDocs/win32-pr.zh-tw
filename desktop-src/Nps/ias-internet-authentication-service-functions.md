---
title: NPS 擴充功能函式
description: NPS 擴充功能函式
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "107001283"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="c6de7-103">NPS 擴充功能函式</span><span class="sxs-lookup"><span data-stu-id="c6de7-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="c6de7-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="c6de7-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c6de7-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="c6de7-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c6de7-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="c6de7-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="c6de7-107">定義的應用程式</span><span class="sxs-lookup"><span data-stu-id="c6de7-107">Application Defined</span></span>

<span data-ttu-id="c6de7-108">NPS 擴充功能 Dll 的架構支援下列匯出的函式：</span><span class="sxs-lookup"><span data-stu-id="c6de7-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="c6de7-109">**RadiusExtensionFreeAttributes**</span><span class="sxs-lookup"><span data-stu-id="c6de7-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="c6de7-110">**RadiusExtensionInit**</span><span class="sxs-lookup"><span data-stu-id="c6de7-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="c6de7-111">**RadiusExtensionProcess**</span><span class="sxs-lookup"><span data-stu-id="c6de7-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="c6de7-112">**RadiusExtensionProcessEx**</span><span class="sxs-lookup"><span data-stu-id="c6de7-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="c6de7-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="c6de7-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="c6de7-114">**RadiusExtensionTerm**</span><span class="sxs-lookup"><span data-stu-id="c6de7-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="c6de7-115">[**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init)和 [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term)函數是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="c6de7-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="c6de7-116">延伸模組 DLL 可以匯出 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) ，而不是 [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) 或 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)。</span><span class="sxs-lookup"><span data-stu-id="c6de7-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="c6de7-117">如果延伸模組 DLL 匯出 [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)，則它也必須匯出 [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)。</span><span class="sxs-lookup"><span data-stu-id="c6de7-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="c6de7-118">系統定義</span><span class="sxs-lookup"><span data-stu-id="c6de7-118">System Defined</span></span>

<span data-ttu-id="c6de7-119">當 NPS 呼叫 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)的執行時，nps 會將指標傳遞至 [**RADIUS \_ 延伸 \_ \_ 模組控制區塊**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c6de7-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="c6de7-120">[**RADIUS \_ 延伸 \_ 模組控制 \_ 區塊**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block)結構包含 NPS 所提供之下列函式的函式指標：</span><span class="sxs-lookup"><span data-stu-id="c6de7-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="c6de7-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="c6de7-124">[**GetRequest**](/previous-versions/ms688263(v=vs.85))和 [**GetResponse**](/previous-versions/ms688270(v=vs.85))函式會傳回 [**RADIUS \_ 屬性 \_ 陣列**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)類型之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c6de7-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="c6de7-125">[**RADIUS \_ 屬性 \_ 陣列**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)結構包含 NPS 所提供之下列函式的函式指標：</span><span class="sxs-lookup"><span data-stu-id="c6de7-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="c6de7-126">[**加入**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="c6de7-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6de7-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 