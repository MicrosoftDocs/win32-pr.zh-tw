---
description: 附件嵌入式管理單元延伸模組是顯示服務特定使用者介面之附件的元件。
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: 附件嵌入式管理單元擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997321"
---
# <a name="attachment-snap-in-extensions"></a><span data-ttu-id="3633a-103">附件嵌入式管理單元擴充功能</span><span class="sxs-lookup"><span data-stu-id="3633a-103">Attachment Snap-in Extensions</span></span>

<span data-ttu-id="3633a-104">附件嵌入式管理單元延伸模組是顯示服務特定使用者介面之附件的元件。</span><span class="sxs-lookup"><span data-stu-id="3633a-104">An attachment snap-in extension is the component of an attachment that displays the service-specific user interface.</span></span> <span data-ttu-id="3633a-105">此嵌入式管理單元的擴充功能是由安全性設定嵌入式管理單元所主控。附件延伸模組與其嵌入式管理單元主機之間的通訊，是由 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔中所述的標準 MMC 機制所處理。</span><span class="sxs-lookup"><span data-stu-id="3633a-105">The snap-in extension is hosted by the Security Configuration snap-ins. The communication between the attachment extension and its snap-in host is handled by the standard MMC mechanisms described in the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="3633a-106">除了嵌入式管理單元延伸模組必須支援的介面才能成為 MMC 嵌入式管理單元擴充功能之外，附件嵌入式管理單元延伸模組也必須支援 COM 介面 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)。</span><span class="sxs-lookup"><span data-stu-id="3633a-106">In addition to the interfaces that the snap-in extension must support in order to be an MMC snap-in extension, an attachment snap-in extension must also support the COM interface, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="3633a-107">這個介面會執行方法，指出是否有應儲存至安全性資料庫的服務特定資料，如果是，則會取出並儲存這項新資料。</span><span class="sxs-lookup"><span data-stu-id="3633a-107">This interface implements methods that indicate whether there is service-specific data that should be saved to the security database, and if so, retrieve and save this new data.</span></span> <span data-ttu-id="3633a-108">[安全性設定] 嵌入式管理單元會定期呼叫此介面的方法，以便更新安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="3633a-108">The Security Configuration snap-ins call methods of this interface regularly in order to update the security database.</span></span>

<span data-ttu-id="3633a-109">[安全性設定] 嵌入式管理單元會執行介面 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)，以提供從安全性資料庫取出服務特定資料的方法。</span><span class="sxs-lookup"><span data-stu-id="3633a-109">The Security Configuration snap-ins implement an interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), that provides methods to retrieve service-specific data from the security database.</span></span> <span data-ttu-id="3633a-110">附件嵌入式管理單元擴充功能可以呼叫這個介面的方法，從安全性資料庫中取出資料。</span><span class="sxs-lookup"><span data-stu-id="3633a-110">Attachment snap-in extensions can call methods of this interface to retrieve data from the security database.</span></span>

<span data-ttu-id="3633a-111">下圖說明此架構。</span><span class="sxs-lookup"><span data-stu-id="3633a-111">This architecture is illustrated in the following diagram.</span></span>

![附件嵌入式管理單元擴充功能](images/model2.png)

<span data-ttu-id="3633a-113">當您建立附件嵌入式管理單元延伸模組時，您必須加以安裝，並使用 [安全性設定] 嵌入式管理單元來註冊它。若要這麼做，請將機碼新增到登錄中，如 [註冊附件嵌入式管理單元擴充功能](registering-an-attachment-snap-in-extension.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="3633a-113">When you create an attachment snap-in extension, you must install it and register it with the Security Configuration snap-ins. You do this by adding keys to the registry, as explained in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span> <span data-ttu-id="3633a-114">當安全性設定嵌入式管理單元開始時，它會檢查登錄並載入任何已註冊的嵌入式管理單元擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3633a-114">When a Security Configuration snap-in starts, it checks the registry and loads any registered snap-in extensions.</span></span> <span data-ttu-id="3633a-115">延伸模組會在 [安全性設定] 嵌入式管理單元中，顯示為每個服務的 [安全性] 區域下的節點。</span><span class="sxs-lookup"><span data-stu-id="3633a-115">The extensions appear as nodes under the security area for each service in the Security Configuration snap-in.</span></span>

> [!Note]
> <span data-ttu-id="3633a-116">附件嵌入式管理單元延伸模組只能擴充服務節點。</span><span class="sxs-lookup"><span data-stu-id="3633a-116">An attachment snap-in extension can only extend Services nodes.</span></span> <span data-ttu-id="3633a-117">[服務] 節點是 MMC 嵌入式管理單元，其中包含的工具可用來管理系統上安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="3633a-117">The Services node is the MMC snap-in that contains tools to administer services installed on the system.</span></span> <span data-ttu-id="3633a-118">附件嵌入式管理單元延伸模組會將本身宣告為特定服務節點類型的次級，然後針對該服務節點類型的每個出現專案，MMC 主控台會自動新增相關的嵌入式管理單元擴充功能。</span><span class="sxs-lookup"><span data-stu-id="3633a-118">The attachment snap-in extension declares itself as being a subordinate to a specific Services node type, and then for each occurrence of that Services node type, the MMC console automatically adds the related snap-in extensions.</span></span>
> 
> <span data-ttu-id="3633a-119">每個附件嵌入式管理單元延伸模組都擁有一個 [領域] 窗格節點，以及 MMC 中的 [相關結果] 窗格。</span><span class="sxs-lookup"><span data-stu-id="3633a-119">Each attachment snap-in extension owns one scope pane node and the related result pane in MMC.</span></span>

 

 

 
