---
title: '登錄專案 (COM) '
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 深入瞭解： (COM) 的登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111453"
---
# <a name="registry-entries-com"></a><span data-ttu-id="a7816-103">登錄專案 (COM) </span><span class="sxs-lookup"><span data-stu-id="a7816-103">Registry Entries (COM)</span></span>

<span data-ttu-id="a7816-104">下列登錄機碼中的登錄值會控制 COM 功能的各個層面：</span><span class="sxs-lookup"><span data-stu-id="a7816-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="a7816-105">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別**</span><span class="sxs-lookup"><span data-stu-id="a7816-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="a7816-106">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Ole**</span><span class="sxs-lookup"><span data-stu-id="a7816-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="a7816-107">**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="a7816-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="a7816-108">從 Windows Server 2003，COM 只會使用目前的進程權杖來決定要存取的登錄區，而不是執行緒 token。</span><span class="sxs-lookup"><span data-stu-id="a7816-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="a7816-109">如果 COM 無法存取使用者設定檔登錄區，它將會存取 **HKEY \_ 本機 \_ 電腦 \\ 系統** hive。</span><span class="sxs-lookup"><span data-stu-id="a7816-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7816-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7816-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7816-111">登錄</span><span class="sxs-lookup"><span data-stu-id="a7816-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
