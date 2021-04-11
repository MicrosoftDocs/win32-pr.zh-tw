---
description: 圖形 API 會使用下列回呼：
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: 圖形 API 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026754"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="008a0-103">圖形 API 回呼</span><span class="sxs-lookup"><span data-stu-id="008a0-103">Graphing API Callbacks</span></span>

<span data-ttu-id="008a0-104">圖形 API 會使用下列回呼：</span><span class="sxs-lookup"><span data-stu-id="008a0-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="008a0-105">回呼</span><span class="sxs-lookup"><span data-stu-id="008a0-105">Callback</span></span>                                                          | <span data-ttu-id="008a0-106">Description</span><span class="sxs-lookup"><span data-stu-id="008a0-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="008a0-107">*PFNPEER \_ 免費的 \_ 安全性 \_ 資料*</span><span class="sxs-lookup"><span data-stu-id="008a0-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="008a0-108">指定對等圖形基礎結構呼叫的函式，以釋放 [*PFNPEER \_ SECURE \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) 和 [*PFNPEER \_ VALIDATE \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) 回呼所傳回的資料。</span><span class="sxs-lookup"><span data-stu-id="008a0-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="008a0-109">*PFNPEER \_ 安全 \_ 記錄*</span><span class="sxs-lookup"><span data-stu-id="008a0-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="008a0-110">指定對等圖形基礎結構呼叫以保護記錄的函式。</span><span class="sxs-lookup"><span data-stu-id="008a0-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="008a0-111">*PFNPEER \_ 驗證 \_ 記錄*</span><span class="sxs-lookup"><span data-stu-id="008a0-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="008a0-112">指定對等圖形基礎結構呼叫以驗證記錄的函式。</span><span class="sxs-lookup"><span data-stu-id="008a0-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



