---
description: 網路檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。 檔案功能如下所示。
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: " (網路共用管理) 的 NetFile 函式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980628"
---
# <a name="netfile-functions-network-share-management"></a><span data-ttu-id="dd839-104"> (網路共用管理) 的 NetFile 函式</span><span class="sxs-lookup"><span data-stu-id="dd839-104">NetFile Functions (Network Share Management)</span></span>

<span data-ttu-id="dd839-105">網路檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。</span><span class="sxs-lookup"><span data-stu-id="dd839-105">The network file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="dd839-106">檔案功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="dd839-106">The file functions are listed following.</span></span>



| <span data-ttu-id="dd839-107">函式</span><span class="sxs-lookup"><span data-stu-id="dd839-107">Function</span></span>                                 | <span data-ttu-id="dd839-108">描述</span><span class="sxs-lookup"><span data-stu-id="dd839-108">Description</span></span>                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="dd839-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="dd839-109">**NetFileClose**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="dd839-110">強制關閉資源。</span><span class="sxs-lookup"><span data-stu-id="dd839-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="dd839-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="dd839-111">**NetFileEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="dd839-112">傳回伺服器上開啟之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd839-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="dd839-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="dd839-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="dd839-114">傳回伺服器資源特定開啟的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd839-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="dd839-115">當檔案無法以任何其他方式關閉時，請呼叫 [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) 函式。</span><span class="sxs-lookup"><span data-stu-id="dd839-115">Call the [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="dd839-116">因為 **NetFileClose** 不會在關閉檔案之前將用戶端系統上快取的資料寫入至檔案，所以應謹慎使用這個函數。</span><span class="sxs-lookup"><span data-stu-id="dd839-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="dd839-117">[**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)函數會傳回在伺服器上開啟之資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd839-117">The [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="dd839-118">一個或多個應用程式可以開啟一或多次檔案。</span><span class="sxs-lookup"><span data-stu-id="dd839-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="dd839-119">每個檔案開啟都會唯一識別。</span><span class="sxs-lookup"><span data-stu-id="dd839-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="dd839-120">**NetFileEnum** 函式會傳回每個開啟檔案的專案。</span><span class="sxs-lookup"><span data-stu-id="dd839-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="dd839-121">[**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo)函式會傳回一次開啟資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd839-121">The [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="dd839-122">檔案資訊可在下列層級使用。</span><span class="sxs-lookup"><span data-stu-id="dd839-122">File information is available at the following levels.</span></span>

<dl>

[<span data-ttu-id="dd839-123">**檔案 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="dd839-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[<span data-ttu-id="dd839-124">**檔案 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="dd839-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

<span data-ttu-id="dd839-125">不支援層級0和1。</span><span class="sxs-lookup"><span data-stu-id="dd839-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="dd839-126">層級2只會傳回在開啟時指派給資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd839-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="dd839-127">層級3會傳回識別碼、許可權、檔案鎖定，以及開啟資源之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd839-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="dd839-128">如果您要針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以達到您可以藉由呼叫 [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) 和 [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) 函式達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="dd839-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="dd839-129">如需詳細資訊，請參閱 [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) 和 [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)。</span><span class="sxs-lookup"><span data-stu-id="dd839-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
