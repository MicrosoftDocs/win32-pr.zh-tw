---
description: 憑證可以透過任何傳輸機制來要求和散發。
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: 傳輸獨立性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969224"
---
# <a name="transport-independence"></a><span data-ttu-id="de6b8-103">傳輸獨立性</span><span class="sxs-lookup"><span data-stu-id="de6b8-103">Transport Independence</span></span>

<span data-ttu-id="de6b8-104">憑證可以透過任何傳輸機制來要求和散發。</span><span class="sxs-lookup"><span data-stu-id="de6b8-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="de6b8-105">憑證服務會透過 HTTP、DCOM、RPC、磁片檔案或自訂傳輸，接受來自申請者的 [*憑證要求*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="de6b8-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="de6b8-106">憑證服務會透過 HTTP、DCOM、RPC、磁片檔案或自訂傳輸，將憑證張貼到申請者。</span><span class="sxs-lookup"><span data-stu-id="de6b8-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="de6b8-107">中繼應用程式和結束模組 Dll 都支援傳輸，通常是以 C/c + + 撰寫。</span><span class="sxs-lookup"><span data-stu-id="de6b8-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="de6b8-108">中繼應用程式和結束模組會隔離憑證服務功能，而不是與任何特定傳輸通訊。</span><span class="sxs-lookup"><span data-stu-id="de6b8-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
