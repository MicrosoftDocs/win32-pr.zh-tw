---
description: 從 MTS 手動轉換
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: 從 MTS 手動轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688827"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="5bfae-103">從 MTS 手動轉換</span><span class="sxs-lookup"><span data-stu-id="5bfae-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="5bfae-104">您可能會想要隔離將 MTS 套件轉換為 COM + 應用程式，使其不在 Windows 安裝程式的範圍內。</span><span class="sxs-lookup"><span data-stu-id="5bfae-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="5bfae-105">下列程式提供另一種方法：</span><span class="sxs-lookup"><span data-stu-id="5bfae-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="5bfae-106">使用 MTS 2.0 套件匯出功能來匯出 MTS 套件， (產生 MTS 套件檔案和其他檔案的集合) 。</span><span class="sxs-lookup"><span data-stu-id="5bfae-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="5bfae-107">刪除 MTS 套件及升級 Windows，或執行 Windows 的全新安裝。</span><span class="sxs-lookup"><span data-stu-id="5bfae-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="5bfae-108">使用 [元件服務] 系統管理工具的 [應用程式安裝] 嚮導，在 Windows 2000 或更新版本的系統上安裝 MTS 套件 ( pak) 檔案。</span><span class="sxs-lookup"><span data-stu-id="5bfae-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="5bfae-109">您也必須在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ APPID \\ RunAs** 的系統登錄中，重設應用程式的「執行身分」身分識別。</span><span class="sxs-lookup"><span data-stu-id="5bfae-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="5bfae-110">只有自動轉換程式 (透過 Windows 安裝程式或執行 MTSTOCOM 公用程式) 產生 MTSTOCOM 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5bfae-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="5bfae-111">遵循手動轉換程式時，不會產生此檔案。</span><span class="sxs-lookup"><span data-stu-id="5bfae-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5bfae-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bfae-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bfae-113">從 MTS 自動轉換</span><span class="sxs-lookup"><span data-stu-id="5bfae-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="5bfae-114">COM + 轉換結果和問題</span><span class="sxs-lookup"><span data-stu-id="5bfae-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="5bfae-115">MTS 管理程式庫</span><span class="sxs-lookup"><span data-stu-id="5bfae-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



