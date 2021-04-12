---
description: 資源保護可防止取代作業系統檔案和資料夾，以及作業系統的必要登錄機碼。 修改受保護的資源可能會導致應用程式或系統失敗。
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319863"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="bb66b-104">Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="bb66b-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="bb66b-105">目的</span><span class="sxs-lookup"><span data-stu-id="bb66b-105">Purpose</span></span>

<span data-ttu-id="bb66b-106">Windows 資源保護 (WRP) 可防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="bb66b-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="bb66b-107">從 Windows Server 2008 和 Windows Vista 開始，就可以開始使用。</span><span class="sxs-lookup"><span data-stu-id="bb66b-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="bb66b-108">應用程式不應覆寫這些資源，因為系統和其他應用程式會使用這些資源。</span><span class="sxs-lookup"><span data-stu-id="bb66b-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="bb66b-109">保護這些資源可防止應用程式和作業系統失敗。</span><span class="sxs-lookup"><span data-stu-id="bb66b-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="bb66b-110">WRP 是 Windows 檔案保護 (WFP) 的新名稱。</span><span class="sxs-lookup"><span data-stu-id="bb66b-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="bb66b-111">WRP 可保護登錄機碼和資料夾，以及基本的系統檔案。</span><span class="sxs-lookup"><span data-stu-id="bb66b-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="bb66b-112">適用時</span><span class="sxs-lookup"><span data-stu-id="bb66b-112">Where applicable</span></span>

<span data-ttu-id="bb66b-113">所有以 Windows 為基礎的應用程式及其在 Windows Server 2008 或 Windows Vista 及更新版本作業系統上執行的安裝程式，都應該要知道 WRP。</span><span class="sxs-lookup"><span data-stu-id="bb66b-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="bb66b-114">所有在 Microsoft Windows Server 2003 或 Windows XP 上執行的 Windows 應用程式，以及其安裝程式，都應該要知道 WFP。</span><span class="sxs-lookup"><span data-stu-id="bb66b-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bb66b-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="bb66b-115">Developer audience</span></span>

<span data-ttu-id="bb66b-116">WRP API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="bb66b-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="bb66b-117">WRP API 有兩個函式： [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 和 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)。</span><span class="sxs-lookup"><span data-stu-id="bb66b-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bb66b-118">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="bb66b-118">Run-time requirements</span></span>

<span data-ttu-id="bb66b-119">只使用 [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 功能的應用程式需要 windows server 2008、windows Vista、windows server 2003 或 windows XP。</span><span class="sxs-lookup"><span data-stu-id="bb66b-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="bb66b-120">使用 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) 功能的應用程式需要 windows Server 2008 或 windows Vista。</span><span class="sxs-lookup"><span data-stu-id="bb66b-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb66b-121">本節內容</span><span class="sxs-lookup"><span data-stu-id="bb66b-121">In this section</span></span>



| <span data-ttu-id="bb66b-122">主題</span><span class="sxs-lookup"><span data-stu-id="bb66b-122">Topic</span></span>                                                                                     | <span data-ttu-id="bb66b-123">描述</span><span class="sxs-lookup"><span data-stu-id="bb66b-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="bb66b-124">關於 Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="bb66b-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="bb66b-125">關於 WRP 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="bb66b-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="bb66b-126">Windows 資源保護參考</span><span class="sxs-lookup"><span data-stu-id="bb66b-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="bb66b-127">WRP 的參考檔。</span><span class="sxs-lookup"><span data-stu-id="bb66b-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




