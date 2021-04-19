---
description: 下列列舉適用于列印多工緩衝處理器（例如印表機驅動程式和埠監視器）所裝載的應用程式和元件之間的非同步通訊。
ms.assetid: 732a552b-caf9-45da-9a9e-a325c4f6341b
title: 非同步列印通知列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2baf2a4476ac858a883dda55b2864a79d78cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971776"
---
# <a name="asynchronous-printing-notification-enumerations"></a><span data-ttu-id="19d2d-103">非同步列印通知列舉</span><span class="sxs-lookup"><span data-stu-id="19d2d-103">Asynchronous Printing Notification Enumerations</span></span>

<span data-ttu-id="19d2d-104">下列列舉適用于列印多工緩衝處理器（例如印表機驅動程式和埠監視器）所裝載的應用程式和元件之間的非同步通訊。</span><span class="sxs-lookup"><span data-stu-id="19d2d-104">The following enumerations are used in asynchronous communication between applications and components that are hosted by the print spooler, such as printer drivers and port monitors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="19d2d-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="19d2d-105">In this section</span></span>



| <span data-ttu-id="19d2d-106">列舉型別</span><span class="sxs-lookup"><span data-stu-id="19d2d-106">Enumeration</span></span>                                                                               | <span data-ttu-id="19d2d-107">描述</span><span class="sxs-lookup"><span data-stu-id="19d2d-107">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19d2d-108">**PrintAsyncNotifyConversationStyle**</span><span class="sxs-lookup"><span data-stu-id="19d2d-108">**PrintAsyncNotifyConversationStyle**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyconversationstyle)<br/> | <span data-ttu-id="19d2d-109">指定應用程式之間的通訊是雙向或單向的，還是列印多工緩衝處理器裝載的元件，例如印表機驅動程式、列印處理器和埠監視器。</span><span class="sxs-lookup"><span data-stu-id="19d2d-109">Specifies whether communication is bidirectional or unidirectional between applications and Print Spooler-hosted components such as printer drivers, print processors, and port monitors.</span></span><br/>           |
| [<span data-ttu-id="19d2d-110">**PrintAsyncNotifyError**</span><span class="sxs-lookup"><span data-stu-id="19d2d-110">**PrintAsyncNotifyError**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyerror)<br/>                         | <span data-ttu-id="19d2d-111">指定非同步通知失敗後所傳回之 **HRESULT** 的錯誤碼部分。</span><span class="sxs-lookup"><span data-stu-id="19d2d-111">Specifies the error code portion of the **HRESULT** returned after an asynchronous notification failure.</span></span><br/>                                                                                            |
| [<span data-ttu-id="19d2d-112">**PrintAsyncNotifyUserFilter**</span><span class="sxs-lookup"><span data-stu-id="19d2d-112">**PrintAsyncNotifyUserFilter**</span></span>](/windows/desktop/api/prnasnot/ne-prnasnot-printasyncnotifyuserfilter)<br/>               | <span data-ttu-id="19d2d-113">指定通知是否只會傳送給與列印多工緩衝處理器裝載的寄件者相關聯的接聽應用程式，或移至更廣泛的聆聽應用程式集合。</span><span class="sxs-lookup"><span data-stu-id="19d2d-113">Specifies whether notifications will go only to listening applications that are associated with the same user as the Print Spooler-hosted sender, or go to a broader set of listening applications.</span></span><br/> |



 

 

 




