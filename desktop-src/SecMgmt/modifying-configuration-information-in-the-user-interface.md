---
description: 附件嵌入式管理單元延伸模組必須允許使用者修改服務的設定資訊。
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: 修改消費者介面中的設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997895"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a><span data-ttu-id="cb7dd-103">修改消費者介面中的設定資訊</span><span class="sxs-lookup"><span data-stu-id="cb7dd-103">Modifying Configuration Information in the User Interface</span></span>

<span data-ttu-id="cb7dd-104">附件嵌入式管理單元延伸模組必須允許使用者修改服務的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="cb7dd-104">An attachment snap-in extension must allow the user to modify configuration information about the service.</span></span> <span data-ttu-id="cb7dd-105">修改過的資訊應該由附件嵌入式管理單元延伸模組儲存，直到 [安全性設定] 嵌入式管理單元呼叫 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) 介面的方法來取得資訊為止。</span><span class="sxs-lookup"><span data-stu-id="cb7dd-105">The modified information should be stored by the attachment snap-in extension until the Security Configuration snap-in calls methods of the [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interface to retrieve the information.</span></span>

<span data-ttu-id="cb7dd-106">若要避免記憶體流失，請呼叫 [**ISceSvcAttachmentPersistInfo：： FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer)，以釋放嵌入式管理單元擴充功能所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="cb7dd-106">To avoid memory leaks, free memory allocated by the snap-in extension by calling [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).</span></span>

 

 



