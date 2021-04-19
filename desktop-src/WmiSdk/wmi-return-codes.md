---
description: 本節提供 WMI 傳回碼、符號常數、常值和描述的清單。 腳本、c + + 應用程式或 Wmic 命令可能會傳回這些程式碼。
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: WMI 傳回碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980966"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="a5666-104">WMI 傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5666-104">WMI Return Codes</span></span>

<span data-ttu-id="a5666-105">本節提供 WMI 傳回碼、符號常數、常值和描述的清單。</span><span class="sxs-lookup"><span data-stu-id="a5666-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="a5666-106">腳本、c + + 應用程式或 [**Wmic**](wmic.md) 命令可能會傳回這些程式碼。</span><span class="sxs-lookup"><span data-stu-id="a5666-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="a5666-107">如果發生錯誤，WMI 會傳回下列其中一個錯誤碼做為32位值，其中兩個高序位位表示訊息的嚴重性代碼。</span><span class="sxs-lookup"><span data-stu-id="a5666-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="a5666-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="a5666-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="a5666-109">Success</span><span class="sxs-lookup"><span data-stu-id="a5666-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="a5666-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="a5666-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="a5666-111">資訊</span><span class="sxs-lookup"><span data-stu-id="a5666-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="a5666-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="a5666-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="a5666-113">警告</span><span class="sxs-lookup"><span data-stu-id="a5666-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="a5666-114"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="a5666-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="a5666-115">錯誤</span><span class="sxs-lookup"><span data-stu-id="a5666-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="a5666-116">如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。</span><span class="sxs-lookup"><span data-stu-id="a5666-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="a5666-117">失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5666-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="a5666-118">在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a5666-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="a5666-119">若要取得問題來源的詳細資訊，您可以下載並執行 [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) 診斷命令列工具。</span><span class="sxs-lookup"><span data-stu-id="a5666-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="a5666-120">這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。</span><span class="sxs-lookup"><span data-stu-id="a5666-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="a5666-121">報表也會協助 Microsoft 支援服務協助您。</span><span class="sxs-lookup"><span data-stu-id="a5666-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="a5666-122">您可以在 [這裡](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)下載 WMI Diagnosis Utility。</span><span class="sxs-lookup"><span data-stu-id="a5666-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="a5666-123">**WMI 錯誤常數**</span><span class="sxs-lookup"><span data-stu-id="a5666-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="a5666-124">**WMI 非錯誤常數**</span><span class="sxs-lookup"><span data-stu-id="a5666-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



