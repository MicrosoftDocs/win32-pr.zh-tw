---
description: 如果未設定 msidbCustomActionTypeContinue 傳回處理選項，自訂動作必須傳回整數狀態碼，如下表所示。
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: 自訂動作傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971627"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="24c3f-103">自訂動作傳回值</span><span class="sxs-lookup"><span data-stu-id="24c3f-103">Custom Action Return Values</span></span>

<span data-ttu-id="24c3f-104">如果未設定 **msidbCustomActionTypeContinue** 傳回處理選項，自訂動作必須傳回整數狀態碼，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="24c3f-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="24c3f-105">傳回值</span><span class="sxs-lookup"><span data-stu-id="24c3f-105">Return value</span></span>                 | <span data-ttu-id="24c3f-106">描述</span><span class="sxs-lookup"><span data-stu-id="24c3f-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="24c3f-107">\_ \_ 未 \_ 呼叫錯誤函式</span><span class="sxs-lookup"><span data-stu-id="24c3f-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="24c3f-108">未執行動作。</span><span class="sxs-lookup"><span data-stu-id="24c3f-108">Action not executed.</span></span>                  |
| <span data-ttu-id="24c3f-109">錯誤 \_ 成功</span><span class="sxs-lookup"><span data-stu-id="24c3f-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="24c3f-110">已成功完成動作。</span><span class="sxs-lookup"><span data-stu-id="24c3f-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="24c3f-111">\_安裝 \_ USEREXIT 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="24c3f-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="24c3f-112">使用者提前終止。</span><span class="sxs-lookup"><span data-stu-id="24c3f-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="24c3f-113">\_安裝 \_ 失敗時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="24c3f-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="24c3f-114">發生無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="24c3f-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="24c3f-115">\_沒有 \_ 其他 \_ 專案的錯誤</span><span class="sxs-lookup"><span data-stu-id="24c3f-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="24c3f-116">略過其餘的動作，而不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="24c3f-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="24c3f-117">請注意， [可執行檔](executable-files.md) 的自訂動作必須傳回0值才能成功。</span><span class="sxs-lookup"><span data-stu-id="24c3f-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="24c3f-118">安裝程式會將任何其他傳回值視為失敗。</span><span class="sxs-lookup"><span data-stu-id="24c3f-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="24c3f-119">若要忽略傳回值，請在 [CustomAction 資料表](customaction-table.md)的類型欄位中設定 **msidbCustomActionTypeContinue** 位旗標。</span><span class="sxs-lookup"><span data-stu-id="24c3f-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="24c3f-120">如需有關 **msidbCustomActionTypeContinue** 選項和其他傳回處理選項的詳細資訊，請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="24c3f-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="24c3f-121">請注意，Windows Installer 會在將傳回值寫入記錄檔時，轉譯所有動作的傳回值。</span><span class="sxs-lookup"><span data-stu-id="24c3f-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="24c3f-122">例如，如果動作傳回值在記錄檔中顯示為1，這表示動作傳回的錯誤 \_ 成功。</span><span class="sxs-lookup"><span data-stu-id="24c3f-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="24c3f-123">如需此轉譯的詳細資訊，請參閱 [動作傳回值的記錄](logging-of-action-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="24c3f-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24c3f-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="24c3f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24c3f-125">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="24c3f-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="24c3f-126">動作傳回值的記錄</span><span class="sxs-lookup"><span data-stu-id="24c3f-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



