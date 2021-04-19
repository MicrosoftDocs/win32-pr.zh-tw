---
description: 附件嵌入式管理單元擴充功能提供一個介面，讓使用者可用來變更服務特定的設定。
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: 建立附件嵌入式管理單元擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985256"
---
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="c0f9e-103">建立附件嵌入式管理單元擴充功能</span><span class="sxs-lookup"><span data-stu-id="c0f9e-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="c0f9e-104">附件嵌入式管理單元擴充功能提供一個介面，讓使用者可用來變更服務特定的設定。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="c0f9e-105">附件嵌入式管理單元延伸模組必須符合 MMC 需求，才能成為有效的嵌入式管理單元延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="c0f9e-106">如需這些需求的詳細資訊，請參閱 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="c0f9e-107">除了 MMC 所需的介面之外，附件嵌入式管理單元擴充功能還必須執行 COM 介面 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="c0f9e-108">[安全性設定] 嵌入式管理單元會呼叫此介面的方法，以判斷設定資料是否已變更，如果有的話，則會更新安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="c0f9e-109">在 [安全性設定] 嵌入式管理單元抓取該資料之前，[附件] 嵌入式管理單元必須儲存任何設定變更。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="c0f9e-110">附件嵌入式管理單元延伸模組必須提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="c0f9e-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="c0f9e-111">顯示設定和分析資訊</span><span class="sxs-lookup"><span data-stu-id="c0f9e-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="c0f9e-112">修改消費者介面中的設定資訊</span><span class="sxs-lookup"><span data-stu-id="c0f9e-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="c0f9e-113">修改安全性資料庫中的設定資訊</span><span class="sxs-lookup"><span data-stu-id="c0f9e-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="c0f9e-114">為了協助您的嵌入式管理單元擴充功能執行這些工作，安全性設定嵌入式管理單元會執行 COM 介面 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)，以提供您的嵌入式管理單元擴充功能可呼叫的方法，以初始化本身並從安全性資料庫查詢資訊。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="c0f9e-115">建立附件嵌入式管理單元擴充功能之後，您必須使用 [ [註冊附件嵌入式管理](registering-an-attachment-snap-in-extension.md)單元] 延伸模組中所述的 [安全性設定] 嵌入式管理單元來註冊它。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 
