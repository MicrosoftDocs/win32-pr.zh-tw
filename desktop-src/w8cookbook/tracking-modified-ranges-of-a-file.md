---
title: 追蹤檔案的修改範圍
description: 追蹤檔案的修改範圍
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106968517"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="c026d-103">追蹤檔案的修改範圍</span><span class="sxs-lookup"><span data-stu-id="c026d-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="c026d-104">平台</span><span class="sxs-lookup"><span data-stu-id="c026d-104">Platforms</span></span>

<span data-ttu-id="c026d-105">**用戶端-** Windows 8.1 (所有 Sku) </span><span class="sxs-lookup"><span data-stu-id="c026d-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="c026d-106">**伺服器-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c026d-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="c026d-107">Description</span><span class="sxs-lookup"><span data-stu-id="c026d-107">Description</span></span>

<span data-ttu-id="c026d-108">NT 檔案系統 (NTFS) 小組已將新功能新增至 Windows。</span><span class="sxs-lookup"><span data-stu-id="c026d-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="c026d-109">USN 日誌會將更新序號輸出 (USN) 記錄，其中包含關閉時檔案的修改範圍。</span><span class="sxs-lookup"><span data-stu-id="c026d-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="c026d-110">引進了新的記錄類型，已 \_ 引進 USN 記錄 \_ V4 來記錄這些變更的檔案範圍。</span><span class="sxs-lookup"><span data-stu-id="c026d-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="c026d-111">預設不會啟用此功能;使用者必須叫用檔案系統控制項 (FSCTL) 命令才能啟用它。</span><span class="sxs-lookup"><span data-stu-id="c026d-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="c026d-112">不過，因為其他 Windows 元件可能會開啟範圍追蹤，所以使用者和開發人員可能會察覺到功能一律為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="c026d-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="c026d-113">Windows 將可讓開發人員查詢 USN 日誌，以找出範圍追蹤是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="c026d-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="c026d-114">MSDN 檔將于稍後提供，以指示開發人員如何存取 USN \_ 記錄 \_ V4 記錄。</span><span class="sxs-lookup"><span data-stu-id="c026d-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c026d-115">表現</span><span class="sxs-lookup"><span data-stu-id="c026d-115">Manifestation</span></span>

<span data-ttu-id="c026d-116">所有使用 USN 日誌的現有應用程式將繼續正常運作，而不會有任何相容性問題。</span><span class="sxs-lookup"><span data-stu-id="c026d-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 




