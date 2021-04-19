---
description: 從具有設定腳本和 inf 檔案的程式安裝設備磁碟機。 撰寫安裝程式以進行裝置設定和驅動程式安裝。 基於安裝軟體應用程式的目的，不再建議使用此 api。
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: 設定 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980314"
---
# <a name="setup-api"></a><span data-ttu-id="a5602-105">設定 API</span><span class="sxs-lookup"><span data-stu-id="a5602-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="a5602-106">目的</span><span class="sxs-lookup"><span data-stu-id="a5602-106">Purpose</span></span>

<span data-ttu-id="a5602-107">安裝程式 API 會提供一組功能，讓安裝應用程式呼叫來執行安裝作業。</span><span class="sxs-lookup"><span data-stu-id="a5602-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a5602-108">適用時</span><span class="sxs-lookup"><span data-stu-id="a5602-108">Where applicable</span></span>

<span data-ttu-id="a5602-109">您可以使用這些安裝程式來開發安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="a5602-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="a5602-110">安裝程式 API 不應再用來安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="a5602-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="a5602-111">相反地，請使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)開發應用程式安裝程式。</span><span class="sxs-lookup"><span data-stu-id="a5602-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="a5602-112">安裝程式 API 會繼續用來安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="a5602-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="a5602-113">安裝程式 API 適用于桌面樣式應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="a5602-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a5602-114">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="a5602-114">Developer audience</span></span>

<span data-ttu-id="a5602-115">如果開發人員的安裝應用程式需要下列功能，則可以使用安裝程式 API：</span><span class="sxs-lookup"><span data-stu-id="a5602-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="a5602-116">檔案的佇列。</span><span class="sxs-lookup"><span data-stu-id="a5602-116">Queuing of files.</span></span>
-   <span data-ttu-id="a5602-117">檔案的安裝。</span><span class="sxs-lookup"><span data-stu-id="a5602-117">Installation of files.</span></span>
-   <span data-ttu-id="a5602-118">處理安裝錯誤和提示媒體的程式。</span><span class="sxs-lookup"><span data-stu-id="a5602-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="a5602-119">正在更新登錄專案。</span><span class="sxs-lookup"><span data-stu-id="a5602-119">Updating registry entries.</span></span>
-   <span data-ttu-id="a5602-120">記錄檔安裝時進行記錄。</span><span class="sxs-lookup"><span data-stu-id="a5602-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="a5602-121">最近使用的來源路徑的儲存體。</span><span class="sxs-lookup"><span data-stu-id="a5602-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a5602-122">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="a5602-122">Run-time requirements</span></span>

<span data-ttu-id="a5602-123">如需哪些作業系統需要哪些作業系統才能使用特定功能的相關資訊，請參閱函式檔集的需求一節。</span><span class="sxs-lookup"><span data-stu-id="a5602-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a5602-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="a5602-124">In this section</span></span>



| <span data-ttu-id="a5602-125">主題</span><span class="sxs-lookup"><span data-stu-id="a5602-125">Topic</span></span>                                 | <span data-ttu-id="a5602-126">描述</span><span class="sxs-lookup"><span data-stu-id="a5602-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5602-127">概觀</span><span class="sxs-lookup"><span data-stu-id="a5602-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="a5602-128">有關安裝程式 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="a5602-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="a5602-129">參考</span><span class="sxs-lookup"><span data-stu-id="a5602-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="a5602-130">安裝程式 API 資料類型、結構、函數和通知的檔。</span><span class="sxs-lookup"><span data-stu-id="a5602-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

