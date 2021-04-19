---
description: 列出附件引擎提供的介面。
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: 安全性管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979309"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="ae2aa-103">安全性管理介面</span><span class="sxs-lookup"><span data-stu-id="ae2aa-103">Security Management Interfaces</span></span>

<span data-ttu-id="ae2aa-104">本章節包含下列介面群組的參考頁面：</span><span class="sxs-lookup"><span data-stu-id="ae2aa-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="ae2aa-105">附件引擎介面</span><span class="sxs-lookup"><span data-stu-id="ae2aa-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="ae2aa-106">附件引擎介面</span><span class="sxs-lookup"><span data-stu-id="ae2aa-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="ae2aa-107">介面</span><span class="sxs-lookup"><span data-stu-id="ae2aa-107">Interface</span></span>                                                            | <span data-ttu-id="ae2aa-108">描述</span><span class="sxs-lookup"><span data-stu-id="ae2aa-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2aa-109">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="ae2aa-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="ae2aa-110">從 [安全性設定] 嵌入式管理單元抓取指定安全性服務的設定和分析資料。[安全性設定] 嵌入式管理單元會公開這個介面，也就是會呼叫以查詢設定或分析資訊的附件嵌入式管理單元延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ae2aa-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="ae2aa-111">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="ae2aa-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="ae2aa-112">從附件嵌入式管理單元抓取修改過的設定或分析資訊。</span><span class="sxs-lookup"><span data-stu-id="ae2aa-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="ae2aa-113">[安全性設定] 嵌入式管理單元會呼叫這個介面，以從附件嵌入式管理單元擴充功能抓取任何修改過的資訊。</span><span class="sxs-lookup"><span data-stu-id="ae2aa-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="ae2aa-114">然後，[安全性設定] 嵌入式管理單元會將此資料適當地儲存在安全性資料庫中。</span><span class="sxs-lookup"><span data-stu-id="ae2aa-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="ae2aa-115">如需嵌入式管理單元擴充功能必須執行之 COM 介面的詳細資訊，請參閱 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔。</span><span class="sxs-lookup"><span data-stu-id="ae2aa-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
