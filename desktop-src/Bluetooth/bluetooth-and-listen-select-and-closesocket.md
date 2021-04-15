---
title: 藍牙和接聽、選取和導致 closesocket
description: 藍牙使用接聽、選取和導致 closesocket 函式，而不需修改標準的 Windows 通訊端程式設計。
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- 導致 closesocket
- 聆聽
- select
- 藍牙和聆聽
- 藍牙和接聽，請選取
- 藍牙和接聽、選取和導致 closesocket
- 聆聽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463337"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="8a72b-111">藍牙和接聽、選取和導致 closesocket</span><span class="sxs-lookup"><span data-stu-id="8a72b-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="8a72b-112">藍牙使用 [**接聽**](/windows/desktop/api/winsock2/nf-winsock2-listen)、 [**選取**](/windows/desktop/api/winsock2/nf-winsock2-select)和 [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式，而不需修改標準的 Windows 通訊端程式設計。</span><span class="sxs-lookup"><span data-stu-id="8a72b-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="8a72b-113">如同 Windows 通訊端， [**導致 closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) 函式會釋出與通訊端相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="8a72b-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="8a72b-114">呼叫待命函 [](/windows/desktop/api/winsock2/nf-winsock2-listen)式時，強烈建議將低值用於待處理專案（ *backlog* ）參數 (通常是2到 4) ，因為只接受一些用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="8a72b-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="8a72b-115">這會減少配置給接聽通訊端使用的系統資源。</span><span class="sxs-lookup"><span data-stu-id="8a72b-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a72b-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a72b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a72b-117">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="8a72b-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="8a72b-118">**導致 closesocket**</span><span class="sxs-lookup"><span data-stu-id="8a72b-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="8a72b-119">**聽**</span><span class="sxs-lookup"><span data-stu-id="8a72b-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="8a72b-120">**選擇**</span><span class="sxs-lookup"><span data-stu-id="8a72b-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 