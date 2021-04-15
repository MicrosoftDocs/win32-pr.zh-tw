---
description: 大部分的 getXbyY 函式都是由 Ws2 \_32.dll 轉譯為 WSALookupServiceBegin、WSALookupServiceNext 和 WSALookupServiceEnd 序列，其使用一組特殊 guid 作為服務類別。
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: API 中的 GetXbyY 基本方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511465"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="23037-103">API 中的 GetXbyY 基本方法</span><span class="sxs-lookup"><span data-stu-id="23037-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="23037-104">大部分的 **getXbyY** 函式都是由 Ws2 \_32.dll 轉譯為 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)和 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) 序列，其使用一組特殊 guid 作為服務類別。</span><span class="sxs-lookup"><span data-stu-id="23037-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="23037-105">這些 Guid 可識別正在模擬的 **getXbyY** 作業類型。</span><span class="sxs-lookup"><span data-stu-id="23037-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="23037-106">此查詢受限於支援 AF INET 的名稱服務提供者 \_ 。</span><span class="sxs-lookup"><span data-stu-id="23037-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="23037-107">每當 **getXbyY** 函數傳回 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 或 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構時，Ws2 \_32.dll \_ \_ 會在 **LUP** 中指定 WSALookupServiceBegin 傳回 BLOB 旗標，讓名稱服務提供者傳回所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="23037-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="23037-108">這些結構必須稍微修改，因為在中包含的指標必須取代為相對於 blob 資料開頭的位移。</span><span class="sxs-lookup"><span data-stu-id="23037-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="23037-109">當然，這些指標參數所參考的所有值都必須完全包含在 blob 中，而且所有字串都是 ASCII。</span><span class="sxs-lookup"><span data-stu-id="23037-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23037-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="23037-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23037-111">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="23037-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="23037-112">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="23037-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="23037-113">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="23037-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



