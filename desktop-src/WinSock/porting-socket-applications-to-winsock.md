---
description: 本節說明 Winsock 移植考慮。
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: 將通訊端應用程式移植到 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979730"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="7c66f-103">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="7c66f-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="7c66f-104">本節說明 Winsock 移植考慮。</span><span class="sxs-lookup"><span data-stu-id="7c66f-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="7c66f-105">由於 Microsoft Windows 環境中的執行問題，Windows 通訊端已有少數的實例，而這些實例的範圍嚴格遵循 Berkeley 慣例。</span><span class="sxs-lookup"><span data-stu-id="7c66f-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="7c66f-106">當 Windows 通訊端中發生 Berkeley 慣例的偏差時，就會明確且明確地注明偏差。</span><span class="sxs-lookup"><span data-stu-id="7c66f-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="7c66f-107">例如，如果函式是 Windows 通訊端的特定函式，則會使用與下列類似的函數描述中的片語來指定偏差：</span><span class="sxs-lookup"><span data-stu-id="7c66f-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="7c66f-108">函 **\[ 式名稱 \] 函式** 是 Microsoft 特定的 WINDOWS 通訊端 2 API 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7c66f-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="7c66f-109">本節提供將 Berkeley (BSD) UNIX 通訊端應用程式移植到 Winsock 的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="7c66f-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="7c66f-110">通訊端資料類型</span><span class="sxs-lookup"><span data-stu-id="7c66f-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="7c66f-111">Select、FD \_ SET 和 FD \_ XXX 宏</span><span class="sxs-lookup"><span data-stu-id="7c66f-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="7c66f-112">錯誤碼-errno、h \_ errno 和 WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="7c66f-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="7c66f-113">指標</span><span class="sxs-lookup"><span data-stu-id="7c66f-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="7c66f-114">重新命名的函式</span><span class="sxs-lookup"><span data-stu-id="7c66f-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="7c66f-115">支援的通訊端數目上限</span><span class="sxs-lookup"><span data-stu-id="7c66f-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="7c66f-116">包含檔案</span><span class="sxs-lookup"><span data-stu-id="7c66f-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="7c66f-117">函數失敗時傳回值</span><span class="sxs-lookup"><span data-stu-id="7c66f-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="7c66f-118">原始通訊端</span><span class="sxs-lookup"><span data-stu-id="7c66f-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="7c66f-119">位元組順序</span><span class="sxs-lookup"><span data-stu-id="7c66f-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="7c66f-120">擴充 Byte-Order 轉換常式</span><span class="sxs-lookup"><span data-stu-id="7c66f-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="7c66f-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c66f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c66f-122">處理 Winsock 錯誤</span><span class="sxs-lookup"><span data-stu-id="7c66f-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="7c66f-123">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="7c66f-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="7c66f-124">Windows 通訊端錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7c66f-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="7c66f-125">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="7c66f-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



