---
description: 程式設計人員和系統管理員會使用服務設定程式來修改或查詢已安裝服務的資料庫。
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: 服務設定程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112781"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="53e3f-103">服務設定程式</span><span class="sxs-lookup"><span data-stu-id="53e3f-103">Service Configuration Programs</span></span>

<span data-ttu-id="53e3f-104">程式設計人員和系統管理員會使用服務設定程式來修改或查詢已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="53e3f-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="53e3f-105">您也可以使用登錄函數來存取資料庫。</span><span class="sxs-lookup"><span data-stu-id="53e3f-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="53e3f-106">不過，您應該只使用 SCM 設定函數，以確保已正確安裝和設定服務。</span><span class="sxs-lookup"><span data-stu-id="53e3f-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="53e3f-107">SCM 設定函數需要 SCManager 物件的控制碼或服務物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53e3f-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="53e3f-108">若要取得這些控制碼，服務設定程式必須：</span><span class="sxs-lookup"><span data-stu-id="53e3f-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="53e3f-109">您可以使用 [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) 函式來取得指定電腦上之 SCM 資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53e3f-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="53e3f-110">使用 [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) 或 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函數來取得服務物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="53e3f-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="53e3f-111">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="53e3f-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="53e3f-112">服務安裝、移除和列舉</span><span class="sxs-lookup"><span data-stu-id="53e3f-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="53e3f-113">服務設定</span><span class="sxs-lookup"><span data-stu-id="53e3f-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="53e3f-114">使用 SC 設定服務</span><span class="sxs-lookup"><span data-stu-id="53e3f-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



