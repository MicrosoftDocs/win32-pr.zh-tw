---
title: 虛擬通道用戶端註冊
description: 您必須將用戶端 DLL 的名稱儲存在登錄中。
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682506"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="bc4df-103">虛擬通道用戶端註冊</span><span class="sxs-lookup"><span data-stu-id="bc4df-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="bc4df-104">您必須將用戶端 DLL 的名稱儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="bc4df-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="bc4df-105">在登錄中，將子機碼新增至下列其中一個位置：</span><span class="sxs-lookup"><span data-stu-id="bc4df-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="bc4df-106">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **預設** 的 \\ **載入** 宏</span><span class="sxs-lookup"><span data-stu-id="bc4df-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="bc4df-107">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **終端機伺服器用戶端** \\ **連接** \\ **載入** 宏</span><span class="sxs-lookup"><span data-stu-id="bc4df-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="bc4df-108">在登錄路徑中， *連接* 代表連線管理員中的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="bc4df-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="bc4df-109">**\\ 預設的 \\ 載入** 鍵底下的專案會套用至所有連接。</span><span class="sxs-lookup"><span data-stu-id="bc4df-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="bc4df-110">**\\ ***Connection*** \\ Addins** 索引鍵底下的專案只適用于 *連接* 所識別的連接。</span><span class="sxs-lookup"><span data-stu-id="bc4df-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="bc4df-111">您可以使用連線管理員來建立和管理連接。</span><span class="sxs-lookup"><span data-stu-id="bc4df-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="bc4df-112">您可以為子機碼指定任何名稱。</span><span class="sxs-lookup"><span data-stu-id="bc4df-112">The subkey can be given any name.</span></span> <span data-ttu-id="bc4df-113">它必須包含 **reg \_ Sz** 或 **reg \_ EXPAND \_ sz** 值，而且可以選擇性地包含 **reg \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="bc4df-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="bc4df-114">**Reg \_ Sz** 或 **reg \_ 展開 \_ SZ** 值的語法如下所示。</span><span class="sxs-lookup"><span data-stu-id="bc4df-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="bc4df-115">如果 **Name** 是 **REG \_ EXPAND \_ SZ** 值，它可以包含展開于執行時間的未展開環境變數。</span><span class="sxs-lookup"><span data-stu-id="bc4df-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="bc4df-116">*DLLname* 的值可以是完整路徑。</span><span class="sxs-lookup"><span data-stu-id="bc4df-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="bc4df-117">如果 *DLLname* 不包含路徑，則會使用標準 DLL 搜尋策略。</span><span class="sxs-lookup"><span data-stu-id="bc4df-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="bc4df-118">如需詳細資訊，請參閱 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)的備註一節。</span><span class="sxs-lookup"><span data-stu-id="bc4df-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 