---
description: 從 MTS 自動轉換
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: 從 MTS 自動轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111049"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="36310-103">從 MTS 自動轉換</span><span class="sxs-lookup"><span data-stu-id="36310-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="36310-104">自動轉換會以兩個步驟進行，如下所示：</span><span class="sxs-lookup"><span data-stu-id="36310-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="36310-105">在 Windows 安裝期間。</span><span class="sxs-lookup"><span data-stu-id="36310-105">During Windows setup.</span></span> <span data-ttu-id="36310-106">轉換是透過 MTSTOCOM 公用程式，由 Windows 安裝程式處理。</span><span class="sxs-lookup"><span data-stu-id="36310-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="36310-107">如果步驟1失敗，部分或所有的 MTS 套件實際上可能已轉換，但可能遺漏某些屬性。</span><span class="sxs-lookup"><span data-stu-id="36310-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="36310-108">在此情況下，請使用 [元件服務] 系統管理工具來確認所有屬性。</span><span class="sxs-lookup"><span data-stu-id="36310-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="36310-109">MTS 屬性仍會存在於 HKEY \_ 本機電腦 Microsoft 交易) 伺服器之 system registry (的電腦上， \_ \\ \\ 但只能透過 regedit.exe 公用程式存取。</span><span class="sxs-lookup"><span data-stu-id="36310-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="36310-110">在 [Windows 登入] 對話方塊顯示之前最後一次重新開機之後。</span><span class="sxs-lookup"><span data-stu-id="36310-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="36310-111">步驟2會處理需要網路存取的轉換動作， (主要是角色成員建立) 。</span><span class="sxs-lookup"><span data-stu-id="36310-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="36310-112">如果步驟2因為暫時性網路或網域控制站) 失敗而失敗 (，就可以多次重新執行 MTSTOCOM 轉換公用程式。</span><span class="sxs-lookup"><span data-stu-id="36310-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="36310-113">若要這樣做，請在命令提示字元中，或從 [**開始**] 功能表選取 [**執行**] 之後，輸入下列命令： **% windir% \\ system32 \\mtstocom.exe**。</span><span class="sxs-lookup"><span data-stu-id="36310-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="36310-114">MTSTOCOM 記錄檔</span><span class="sxs-lookup"><span data-stu-id="36310-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="36310-115">MTSTOCOM 公用程式會在 Windows 目錄中產生記錄檔 (Mtstocom) 。</span><span class="sxs-lookup"><span data-stu-id="36310-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="36310-116">此記錄檔會保留從 MTS 套件轉換為 COM + 應用程式的記錄。</span><span class="sxs-lookup"><span data-stu-id="36310-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="36310-117">如果轉換過程中有任何錯誤，最好檢查記錄檔以取得進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="36310-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="36310-118">記錄檔會攔截常見的問題，例如不正確使用者或密碼。</span><span class="sxs-lookup"><span data-stu-id="36310-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36310-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="36310-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36310-120">COM + 轉換結果和問題</span><span class="sxs-lookup"><span data-stu-id="36310-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="36310-121">從 MTS 手動轉換</span><span class="sxs-lookup"><span data-stu-id="36310-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="36310-122">MTS 管理程式庫</span><span class="sxs-lookup"><span data-stu-id="36310-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



