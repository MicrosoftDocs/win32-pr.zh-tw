---
description: 您的嵌入式管理單元延伸模組必須向使用者顯示目前的設定和分析資訊。
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: 顯示設定和分析資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979264"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="4d466-103">顯示設定和分析資訊</span><span class="sxs-lookup"><span data-stu-id="4d466-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="4d466-104">您的嵌入式管理單元延伸模組必須向使用者顯示目前的設定和分析資訊。</span><span class="sxs-lookup"><span data-stu-id="4d466-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="4d466-105">若要顯示資訊，[附件嵌入式管理單元擴充功能] 節點必須使用 [服務] 節點擴充安全性設定嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="4d466-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="4d466-106">[服務] 節點是 MMC 嵌入式管理單元，可管理系統上安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="4d466-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="4d466-107">可以擴充的節點類型如下所示：</span><span class="sxs-lookup"><span data-stu-id="4d466-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="4d466-108">設定服務 NodeType = {24a7f717-1f0c-11d1-affb-00c04fb984f9}</span><span class="sxs-lookup"><span data-stu-id="4d466-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="4d466-109">檢查服務 NodeType = {678050c7-1ff8-11d1-affb-00c04fb984f9}</span><span class="sxs-lookup"><span data-stu-id="4d466-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="4d466-110">展開 [服務] 節點時，MMC 會通知所有已註冊的嵌入式管理單元擴充功能。</span><span class="sxs-lookup"><span data-stu-id="4d466-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="4d466-111">每個附件嵌入式管理單元都應該在 [服務] 節點下插入自己，然後執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="4d466-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="4d466-112">呼叫 **QueryInterface** 以取得安全性設定嵌入式管理單元所公開之 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4d466-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="4d466-113">呼叫 [**ISceSvcAttachmentData：： Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) 以通知安全性設定嵌入式管理單元，嵌入式管理單元延伸模組已載入，以及建立通訊的內容。</span><span class="sxs-lookup"><span data-stu-id="4d466-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="4d466-114">呼叫 [**ISceSvcAttachmentData：：**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) ，以從資料庫取出設定資訊。</span><span class="sxs-lookup"><span data-stu-id="4d466-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="4d466-115">當嵌入式管理單元延伸模組自行初始化或使用者開啟其節點時，就可以執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="4d466-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="4d466-116">如需詳細資訊，請參閱 [新增附件嵌入式管理單元擴充功能節點](adding-an-attachment-snap-in-extension-node.md)。</span><span class="sxs-lookup"><span data-stu-id="4d466-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



