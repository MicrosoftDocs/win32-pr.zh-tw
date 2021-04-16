---
description: TAPI Dll 以及 TAPI 伺服器 (Tapisvr.exe) ，都是將終端使用者或伺服器應用程式與服務提供者分隔的重要抽象概念。 與 TAPI 伺服器搭配的 TAPI DLL 在這兩層之間提供一致的介面。
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551613"
---
# <a name="tapi-dll"></a><span data-ttu-id="208f1-104">TAPI DLL</span><span class="sxs-lookup"><span data-stu-id="208f1-104">TAPI DLL</span></span>

<span data-ttu-id="208f1-105">TAPI Dll 以及 TAPI 伺服器 (Tapisvr.exe) ，都是將終端使用者或伺服器應用程式與服務提供者分隔的重要抽象概念。</span><span class="sxs-lookup"><span data-stu-id="208f1-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="208f1-106">與 TAPI 伺服器搭配的 TAPI DLL 在這兩層之間提供一致的介面。</span><span class="sxs-lookup"><span data-stu-id="208f1-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="208f1-107">TAPI 應用程式會將適當的 DLL 載入其進程空間。</span><span class="sxs-lookup"><span data-stu-id="208f1-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="208f1-108">在初始化期間，TAPI 會建立與 Tapisvr.exe 的 RPC 連結。</span><span class="sxs-lookup"><span data-stu-id="208f1-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="208f1-109">TAPI 伺服器是在 SVCHOST 的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="208f1-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="208f1-110">有三個與 TAPI 相關聯的 Dll： Tapi.dll、Tapi32.dll 和 Tapi3.dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="208f1-111">這些 Dll 位於% SystemRoot% system32 中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="208f1-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="208f1-112">下圖說明在 Microsoft 電話語音中各自角色的角色：</span><span class="sxs-lookup"><span data-stu-id="208f1-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![三個 tapi dll 的角色](images/dllserv.png)

<span data-ttu-id="208f1-114">現有的16位應用程式連結至 Tapi.dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="208f1-115">Tapi.dll 只是一個 Thunk 層，可將16位位址對應到32位位址，並將要求傳遞給 Tapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="208f1-116">現有的32位 TAPI 2.x 應用程式會連結至 Tapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="208f1-117">Tapi32.dll 是一種精簡的封送處理層，可將函式要求傳輸至 TAPI 伺服器 (TAPISRV) 並且在需要時，在應用程式的進程中載入及叫用媒體服務提供者 Dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="208f1-118">TAPI 2.x 應用程式會連結至 Tapi3.dll。</span><span class="sxs-lookup"><span data-stu-id="208f1-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



