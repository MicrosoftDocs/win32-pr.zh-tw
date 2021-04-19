---
description: ICE39 會驗證資料庫的摘要資訊資料流程。
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979900"
---
# <a name="ice39"></a><span data-ttu-id="657c6-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="657c6-103">ICE39</span></span>

<span data-ttu-id="657c6-104">ICE39 會驗證資料庫的 [摘要資訊資料流程](summary-information-stream.md) 。</span><span class="sxs-lookup"><span data-stu-id="657c6-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="657c6-105">ICE39 會檢查下列屬性的格式：</span><span class="sxs-lookup"><span data-stu-id="657c6-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="657c6-106">**字數統計摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="657c6-107">**頁面計數摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="657c6-108">**範本摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="657c6-109">**修訂編號摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="657c6-110">**建立時間/日期摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="657c6-111">**上次儲存的時間/日期摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="657c6-112">**上次列印的摘要**</span><span class="sxs-lookup"><span data-stu-id="657c6-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="657c6-113">如果 [ [**字數統計摘要**](word-count-summary.md) ] 屬性指定要壓縮來源，ICE39 會在檔案 [資料表](file-table.md)的 [屬性] 資料行中將任何檔案標示為已壓縮時，張貼警告。</span><span class="sxs-lookup"><span data-stu-id="657c6-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="657c6-114">請參閱 [使用封包和壓縮的來源](using-cabinets-and-compressed-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="657c6-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="657c6-115">如果 [ [**字數統計**](word-count-summary.md) ] 屬性指定封裝符合 UAC 規範，且 [MsiPackageCertificate 資料表](msipackagecertificate-table.md) 不是空的，ICE39 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="657c6-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="657c6-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="657c6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="657c6-117">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="657c6-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



