---
title: WebDAV API 結構
description: WebDAV API 中會使用下列結構。
ms.assetid: 1fa7b740-ac93-4756-ac9f-6a8cb4ea8bc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abe54d58ef03bc8057336cb0e4bbbe3e833fb59c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315796"
---
# <a name="webdav-api-structures"></a><span data-ttu-id="82d26-103">WebDAV API 結構</span><span class="sxs-lookup"><span data-stu-id="82d26-103">WebDAV API Structures</span></span>

<span data-ttu-id="82d26-104">WebDAV API 中會使用下列結構。</span><span class="sxs-lookup"><span data-stu-id="82d26-104">The following structures are used in the WebDAV API.</span></span>



| <span data-ttu-id="82d26-105">結構</span><span class="sxs-lookup"><span data-stu-id="82d26-105">Structure</span></span>                                                   | <span data-ttu-id="82d26-106">Description</span><span class="sxs-lookup"><span data-stu-id="82d26-106">Description</span></span>                                                                                                                                                                                         |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82d26-107">**DAV \_ 回呼 \_ 驗證 \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="82d26-107">**DAV\_CALLBACK\_AUTH\_BLOB**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_blob) | <span data-ttu-id="82d26-108">此結構是用來儲存 [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)回呼函式所取出的驗證 [*BLOB*](/windows/desktop/SecGloss/b-gly) 。</span><span class="sxs-lookup"><span data-stu-id="82d26-108">This structure is used to store an authentication [*BLOB*](/windows/desktop/SecGloss/b-gly) that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span> |
| [<span data-ttu-id="82d26-109">**DAV \_ 回呼 \_ 驗證 \_ UNP**</span><span class="sxs-lookup"><span data-stu-id="82d26-109">**DAV\_CALLBACK\_AUTH\_UNP**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_auth_unp)   | <span data-ttu-id="82d26-110">此結構是用來儲存 [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) 回呼函式所取出的使用者名稱和密碼資訊。</span><span class="sxs-lookup"><span data-stu-id="82d26-110">This structure is used to store user name and password information that was retrieved by the [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function.</span></span>                                               |
| [<span data-ttu-id="82d26-111">**DAV \_ 回呼 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="82d26-111">**DAV\_CALLBACK\_CRED**</span></span>](/windows/desktop/api/Davclnt/ns-davclnt-dav_callback_cred)            | <span data-ttu-id="82d26-112">[*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)回呼函式會使用此結構來儲存使用者認證資訊。</span><span class="sxs-lookup"><span data-stu-id="82d26-112">The [*DavAuthCallback*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) callback function uses this structure to store user credential information.</span></span>                                                                               |



 

 

 