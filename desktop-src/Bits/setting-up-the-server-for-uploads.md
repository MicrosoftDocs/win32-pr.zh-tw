---
title: 設定伺服器以進行上傳
description: 若要使用 BITS 將檔案上傳到伺服器，伺服器必須已安裝 IIS 和 BITS 伺服器延伸 ISAPI。 如需 IIS 需求，請參閱 IIS 的 BITS 上傳需求。
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183045"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="e59c8-104">設定伺服器以進行上傳</span><span class="sxs-lookup"><span data-stu-id="e59c8-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="e59c8-105">若要使用 BITS 將檔案上傳到伺服器，伺服器必須已安裝 IIS 和 BITS 伺服器延伸 ISAPI。</span><span class="sxs-lookup"><span data-stu-id="e59c8-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="e59c8-106">如需 IIS 需求，請參閱 [iis 的 BITS 上傳需求](iis-requirements-for-bits-uploads.md)。</span><span class="sxs-lookup"><span data-stu-id="e59c8-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="e59c8-107">如需設定 BITS 用於上傳之 IIS 虛擬目錄的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="e59c8-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="e59c8-108">設定虛擬目錄的許可權</span><span class="sxs-lookup"><span data-stu-id="e59c8-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="e59c8-109">撰寫腳本來設定虛擬目錄</span><span class="sxs-lookup"><span data-stu-id="e59c8-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="e59c8-110">使用 IIS UI 來設定虛擬目錄</span><span class="sxs-lookup"><span data-stu-id="e59c8-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="e59c8-111">防止多個上傳</span><span class="sxs-lookup"><span data-stu-id="e59c8-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="e59c8-112">上傳最佳作法</span><span class="sxs-lookup"><span data-stu-id="e59c8-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="e59c8-113">部分 IIS 安裝包含 UrlScan 篩選元件。</span><span class="sxs-lookup"><span data-stu-id="e59c8-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="e59c8-114">如果已啟用 UrlScan，則系統管理員必須將 "BITS \_ POST" 動詞新增至 UrlScan 的允許 HTTP 動詞命令清單。</span><span class="sxs-lookup"><span data-stu-id="e59c8-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="e59c8-115">否則，BITS 用戶端上傳將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e59c8-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="e59c8-116">如需在 UrlScan 中啟用動詞的詳細資訊，請參閱 UrlScan 檔。</span><span class="sxs-lookup"><span data-stu-id="e59c8-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




