---
title: " (網路管理) 的 NetFile 函式"
description: 網路管理檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。 檔案功能如下所示。
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508260"
---
# <a name="netfile-functions-network-management"></a><span data-ttu-id="790b3-104"> (網路管理) 的 NetFile 函式</span><span class="sxs-lookup"><span data-stu-id="790b3-104">NetFile Functions (Network Management)</span></span>

<span data-ttu-id="790b3-105">網路管理檔案功能提供一種方式來監視和關閉在伺服器上開啟的檔案、裝置和管道資源。</span><span class="sxs-lookup"><span data-stu-id="790b3-105">The network management file functions provide a way to monitor and close the file, device, and pipe resources open on a server.</span></span> <span data-ttu-id="790b3-106">檔案功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="790b3-106">The file functions are listed following.</span></span>



| <span data-ttu-id="790b3-107">函式</span><span class="sxs-lookup"><span data-stu-id="790b3-107">Function</span></span>                                | <span data-ttu-id="790b3-108">描述</span><span class="sxs-lookup"><span data-stu-id="790b3-108">Description</span></span>                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="790b3-109">**NetFileClose**</span><span class="sxs-lookup"><span data-stu-id="790b3-109">**NetFileClose**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | <span data-ttu-id="790b3-110">強制關閉資源。</span><span class="sxs-lookup"><span data-stu-id="790b3-110">Forces a resource to close.</span></span>                                          |
| [<span data-ttu-id="790b3-111">**NetFileEnum**</span><span class="sxs-lookup"><span data-stu-id="790b3-111">**NetFileEnum**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | <span data-ttu-id="790b3-112">傳回伺服器上開啟之檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="790b3-112">Returns information about open files on a server.</span></span>                    |
| [<span data-ttu-id="790b3-113">**NetFileGetInfo**</span><span class="sxs-lookup"><span data-stu-id="790b3-113">**NetFileGetInfo**</span></span>](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | <span data-ttu-id="790b3-114">傳回伺服器資源特定開啟的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="790b3-114">Returns information about a particular opening of a server resource.</span></span> |



 

<span data-ttu-id="790b3-115">當檔案無法以任何其他方式關閉時，請呼叫 [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) 函式。</span><span class="sxs-lookup"><span data-stu-id="790b3-115">Call the [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) function when the file cannot be closed by any other means.</span></span> <span data-ttu-id="790b3-116">因為 **NetFileClose** 不會在關閉檔案之前將用戶端系統上快取的資料寫入至檔案，所以應謹慎使用這個函數。</span><span class="sxs-lookup"><span data-stu-id="790b3-116">This function should be used with caution because **NetFileClose** does not write data cached on the client system to the file before closing the file.</span></span>

<span data-ttu-id="790b3-117">[**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)函數會傳回在伺服器上開啟之資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="790b3-117">The [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) function returns information about resources open on a server.</span></span> <span data-ttu-id="790b3-118">一個或多個應用程式可以開啟一或多次檔案。</span><span class="sxs-lookup"><span data-stu-id="790b3-118">A file can be opened one or more times by one or more applications.</span></span> <span data-ttu-id="790b3-119">每個檔案開啟都會唯一識別。</span><span class="sxs-lookup"><span data-stu-id="790b3-119">Each file opening is uniquely identified.</span></span> <span data-ttu-id="790b3-120">**NetFileEnum** 函式會傳回每個開啟檔案的專案。</span><span class="sxs-lookup"><span data-stu-id="790b3-120">The **NetFileEnum** function returns an entry for each file opening.</span></span> <span data-ttu-id="790b3-121">[**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo)函式會傳回一次開啟資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="790b3-121">The [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) function returns information about one opening of a resource.</span></span>

<span data-ttu-id="790b3-122">檔案資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="790b3-122">File information is available at the following levels:</span></span>

-   [<span data-ttu-id="790b3-123">**檔案 \_ 資訊 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="790b3-123">**FILE\_INFO\_2**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [<span data-ttu-id="790b3-124">**檔案 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="790b3-124">**FILE\_INFO\_3**</span></span>](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

<span data-ttu-id="790b3-125">不支援層級0和1。</span><span class="sxs-lookup"><span data-stu-id="790b3-125">Levels 0 and 1 are not supported.</span></span> <span data-ttu-id="790b3-126">層級2只會傳回在開啟時指派給資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="790b3-126">Level 2 returns only the identification number assigned to the resource when it was opened.</span></span> <span data-ttu-id="790b3-127">層級3會傳回識別碼、許可權、檔案鎖定，以及開啟資源之使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="790b3-127">Level 3 returns the identification number, permissions, file locks, and the name of the user who opened the resource.</span></span>

<span data-ttu-id="790b3-128">如果您要針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以達到您可以藉由呼叫 [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) 和 [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) 函式達成的相同功能。</span><span class="sxs-lookup"><span data-stu-id="790b3-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) and [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) functions.</span></span> <span data-ttu-id="790b3-129">如需詳細資訊，請參閱 [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) 和 [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)。</span><span class="sxs-lookup"><span data-stu-id="790b3-129">For more information, see [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
