---
description: 擴充性的達成方式是提供新的物件識別碼 (Oid) 、新的編碼類型和新的 Dll。
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: OID 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850851"
---
# <a name="oid-overview"></a><span data-ttu-id="37d31-103">OID 總覽</span><span class="sxs-lookup"><span data-stu-id="37d31-103">OID Overview</span></span>

<span data-ttu-id="37d31-104">擴充性的達成方式是提供新的 [*物件識別碼*](../secgloss/o-gly.md) (oid) 、新的編碼類型和新的 dll。</span><span class="sxs-lookup"><span data-stu-id="37d31-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="37d31-105">CryptoAPI Oid 可以採用下列任何形式：</span><span class="sxs-lookup"><span data-stu-id="37d31-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="37d31-106">數值字串，例如 "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="37d31-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="37d31-107">英數位元字串，例如 *MyFunction*</span><span class="sxs-lookup"><span data-stu-id="37d31-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="37d31-108">值小於或等於0xFFFF 的常數。</span><span class="sxs-lookup"><span data-stu-id="37d31-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="37d31-109">這些常數通常會透過在標頭檔中使用 **\# define** 語句來與名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="37d31-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="37d31-110">可擴充函式接受 OID 和編碼類型引數。</span><span class="sxs-lookup"><span data-stu-id="37d31-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="37d31-111">這些函式會搜尋系統登錄，以尋找與傳遞給函式的 OID 和編碼類型引數相關聯的 DLL。</span><span class="sxs-lookup"><span data-stu-id="37d31-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="37d31-112">如果已找到 OID 的 DLL、編碼類型組合，就會載入 DLL，並呼叫其函式。</span><span class="sxs-lookup"><span data-stu-id="37d31-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="37d31-113">下圖顯示此 [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) 函式的流程：</span><span class="sxs-lookup"><span data-stu-id="37d31-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![oid 流程](images/oidflow.png)

<span data-ttu-id="37d31-115">這可讓 CryptoAPI 的功能隨著需求而擴充。</span><span class="sxs-lookup"><span data-stu-id="37d31-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="37d31-116">使用此方法會對新功能的開發人員造成負擔，以撰寫該功能的所有必要程式碼。</span><span class="sxs-lookup"><span data-stu-id="37d31-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="37d31-117">例如，若要編碼某些新的資料結構，DLL 中的函數必須執行整個編碼程式。</span><span class="sxs-lookup"><span data-stu-id="37d31-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
