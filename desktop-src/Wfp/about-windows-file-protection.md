---
description: Windows 資源保護 (WRP) 可防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: 關於 Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997913"
---
# <a name="about-windows-resource-protection"></a><span data-ttu-id="d8532-103">關於 Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="d8532-103">About Windows Resource Protection</span></span>

<span data-ttu-id="d8532-104">Windows 資源保護 (WRP) 可防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="d8532-104">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="d8532-105">從 Windows Server 2008 和 Windows Vista 開始，就可以開始使用。</span><span class="sxs-lookup"><span data-stu-id="d8532-105">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="d8532-106">修改受 WRP 保護之資源的完整存取權，僅限 TrustedInstaller。</span><span class="sxs-lookup"><span data-stu-id="d8532-106">Permission for full access to modify WRP-protected resources is restricted to TrustedInstaller.</span></span> <span data-ttu-id="d8532-107">WRP 保護的資源只能使用 [支援的資源取代機制](supported-file-replacement-mechanisms.md) 與 Windows 模組安裝程式服務進行變更。</span><span class="sxs-lookup"><span data-stu-id="d8532-107">WRP-protected resources can only be changed using the [Supported Resource Replacement Mechanisms](supported-file-replacement-mechanisms.md) with the Windows Modules Installer service.</span></span> <span data-ttu-id="d8532-108">保護這些資源可防止應用程式和作業系統失敗。</span><span class="sxs-lookup"><span data-stu-id="d8532-108">Protecting these resources prevents application and operating system failures.</span></span>

<span data-ttu-id="d8532-109">應用程式不應該嘗試修改受 WRP 保護的資源，因為這些資源是由 Windows 和其他應用程式所使用。</span><span class="sxs-lookup"><span data-stu-id="d8532-109">Applications should not attempt to modify WRP-protected resources because these are used by Windows and other applications.</span></span> <span data-ttu-id="d8532-110">如果應用程式嘗試修改受 WRP 保護的資源，則可能會有下列結果。</span><span class="sxs-lookup"><span data-stu-id="d8532-110">If an application attempts to modify a WRP-protected resource, it can have the following results.</span></span>

-   <span data-ttu-id="d8532-111">嘗試取代、修改或刪除重要 Windows 檔案或登錄機碼的應用程式安裝程式可能無法安裝應用程式，並且會收到錯誤訊息，指出已拒絕存取資源。</span><span class="sxs-lookup"><span data-stu-id="d8532-111">Application installers that attempt to replace, modify, or delete critical Windows files or registry keys may fail to install the application and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="d8532-112">嘗試新增或移除子機碼或變更受保護登錄機碼值的應用程式可能會失敗，並會收到錯誤訊息，指出已拒絕存取資源。</span><span class="sxs-lookup"><span data-stu-id="d8532-112">Applications that attempt to add or remove sub-keys or change the values of protected registry keys may fail and will receive an error message stating that access to the resource was denied.</span></span>
-   <span data-ttu-id="d8532-113">依賴將任何資訊寫入受保護登錄機碼、資料夾或檔案的應用程式可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="d8532-113">Applications that rely on writing any information into protected registry keys, folders, or files may fail.</span></span>

<span data-ttu-id="d8532-114">WRP 是 Windows 檔案保護 (WFP) 的新名稱。</span><span class="sxs-lookup"><span data-stu-id="d8532-114">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="d8532-115">WRP 可保護登錄機碼和資料夾，以及基本的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="d8532-115">WRP protects registry keys and folders as well as essential system files.</span></span> <span data-ttu-id="d8532-116">Microsoft Windows Server 2003 和 Windows XP 中有提供 WFP。</span><span class="sxs-lookup"><span data-stu-id="d8532-116">WFP was available in Microsoft Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d8532-117">WRP 取代了 Windows Server 2008 和 Windows Vista 中的 WFP。</span><span class="sxs-lookup"><span data-stu-id="d8532-117">WRP replaces WFP in Windows Server 2008 and Windows Vista.</span></span>

<span data-ttu-id="d8532-118">下列主題將說明 WRP：</span><span class="sxs-lookup"><span data-stu-id="d8532-118">The following topics describe WRP:</span></span>

-   [<span data-ttu-id="d8532-119">受保護的資源清單</span><span class="sxs-lookup"><span data-stu-id="d8532-119">Protected Resource List</span></span>](protected-file-list.md)
-   [<span data-ttu-id="d8532-120">偵測資源取代</span><span class="sxs-lookup"><span data-stu-id="d8532-120">Detecting Resource Replacement</span></span>](detecting-file-replacement.md)
-   [<span data-ttu-id="d8532-121">支援的資源取代機制</span><span class="sxs-lookup"><span data-stu-id="d8532-121">Supported Resource Replacement Mechanisms</span></span>](supported-file-replacement-mechanisms.md)
-   [<span data-ttu-id="d8532-122">系統檔案檢查程式</span><span class="sxs-lookup"><span data-stu-id="d8532-122">System File Checker</span></span>](system-file-checker.md)
-   [<span data-ttu-id="d8532-123">遠端系統管理考慮</span><span class="sxs-lookup"><span data-stu-id="d8532-123">Remote Administration Considerations</span></span>](remote-administration-considerations.md)

 

 



