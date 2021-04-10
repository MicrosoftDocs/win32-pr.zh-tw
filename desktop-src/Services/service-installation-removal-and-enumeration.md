---
description: 設定程式會使用 CreateService 函式，在 SCM 資料庫中安裝新的服務。
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: 服務安裝、移除和列舉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690207"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="98bec-103">服務安裝、移除和列舉</span><span class="sxs-lookup"><span data-stu-id="98bec-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="98bec-104">設定程式會使用 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式，在 SCM 資料庫中安裝新的服務。</span><span class="sxs-lookup"><span data-stu-id="98bec-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="98bec-105">此函數會指定服務的名稱，並提供儲存在資料庫中的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="98bec-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="98bec-106">如需每項服務的資料庫中所儲存資訊的描述，請參閱 [已安裝服務的資料庫](database-of-installed-services.md)。</span><span class="sxs-lookup"><span data-stu-id="98bec-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="98bec-107">如需範例程式碼，請參閱 [安裝服務](installing-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="98bec-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="98bec-108">設定程式會使用 [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) 函式，從資料庫中移除已安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="98bec-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="98bec-109">如需詳細資訊，請參閱 [刪除服務](deleting-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="98bec-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="98bec-110">若要取得服務名稱，請呼叫 [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) 函數。</span><span class="sxs-lookup"><span data-stu-id="98bec-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="98bec-111">您可以藉由呼叫 [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) 函式來取得服務 [控制台] 小程式中所使用的服務顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="98bec-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="98bec-112">服務設定程式可以使用 [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) 函式來列舉所有服務及其狀態。</span><span class="sxs-lookup"><span data-stu-id="98bec-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="98bec-113">它也可以使用 [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) 函數來列舉哪些服務相依于指定的服務物件。</span><span class="sxs-lookup"><span data-stu-id="98bec-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 



