---
description: 大部分的 GetXbyY 函式都是由 Ws2 \_32.dll 轉譯為 WSALookupServiceBegin、WSALookupServiceNext、WSALookupServiceEnd 序列，其使用一組特殊 guid 作為服務類別。
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: SPI 中的 GetXbyY 基本方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848025"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="5512a-103">SPI 中的 GetXbyY 基本方法</span><span class="sxs-lookup"><span data-stu-id="5512a-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="5512a-104">大部分的 **GetXbyY** 函式都是由 Ws2 \_32.dll 轉譯為 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)、 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 序列，其使用一組特殊 guid 作為服務類別。</span><span class="sxs-lookup"><span data-stu-id="5512a-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="5512a-105">這些 Guid 可識別正在模擬的 **GetXbyY** 作業類型。</span><span class="sxs-lookup"><span data-stu-id="5512a-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="5512a-106">此查詢受限於支援 AF INET 的 Nsp \_ 。</span><span class="sxs-lookup"><span data-stu-id="5512a-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="5512a-107">每當 **GetXbyY** 函式傳回 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 或 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構時，Ws2 \_32.dll 將會 \_ \_ 在 **LUP** 中指定 WSALookupServiceBegin 傳回 BLOB 旗標，讓 NSP 傳回所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="5512a-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="5512a-108">這些結構必須稍微修改，因為在中包含的指標必須取代為相對於 blob 資料開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="5512a-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="5512a-109">當然，這些指標成員參考的所有值都必須完全包含在 blob 中，而且所有字串都是 ASCII。</span><span class="sxs-lookup"><span data-stu-id="5512a-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



