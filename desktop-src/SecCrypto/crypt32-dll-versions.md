---
description: Crypt32.dll 是實作為許多 CryptoAPI 函式的模組。
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690139"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="fe136-103">Crypt32.dll 版本</span><span class="sxs-lookup"><span data-stu-id="fe136-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="fe136-104">Crypt32.dll 是在 CryptoAPI 中實作為許多憑證和密碼編譯訊息功能的模組，例如 [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)。</span><span class="sxs-lookup"><span data-stu-id="fe136-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="fe136-105">Crypt32.dll 是 Windows 和 Windows Server 作業系統隨附的模組，但此 DLL 的不同版本會提供不同的功能。</span><span class="sxs-lookup"><span data-stu-id="fe136-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="fe136-106">沒有 API 可判斷使用中的 CryptoAPI 版本，但是您可以使用 [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) 和 [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) 函式來判斷目前正在使用的 Crypt32.dll 版本。</span><span class="sxs-lookup"><span data-stu-id="fe136-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="fe136-107">一般來說，Crypt32.dll 的版本範圍對應至作業系統版本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="fe136-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="fe136-108">不過，此資料表應該僅做為指導方針，因為透過其他更新的方式，Crypt32.dll 版本會與資料表中所示的版本不同。</span><span class="sxs-lookup"><span data-stu-id="fe136-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="fe136-109">Crypt32.dll 版本</span><span class="sxs-lookup"><span data-stu-id="fe136-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="fe136-110">作業系統</span><span class="sxs-lookup"><span data-stu-id="fe136-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe136-111">*版本* >= 5.131.3790。0</span><span class="sxs-lookup"><span data-stu-id="fe136-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="fe136-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe136-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="fe136-113">*版本* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="fe136-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="fe136-114">Windows XP Service Pack 2 (SP2) Windows XP Service Pack 1 (SP1) 與[Q329433](https://support.microsoft.com/kb/329433)的修正程式</span><span class="sxs-lookup"><span data-stu-id="fe136-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="fe136-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe136-115">Windows XP</span></span><br/> |
| <span data-ttu-id="fe136-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="fe136-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="fe136-117">使用 SP1Windows XP 的 Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe136-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
