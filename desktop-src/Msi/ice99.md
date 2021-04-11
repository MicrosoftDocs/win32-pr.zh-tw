---
description: ICE99 會確認目錄資料表中未輸入的屬性名稱會重複保留給 Windows Installer 的公用或私用。
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693335"
---
# <a name="ice99"></a><span data-ttu-id="981a3-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="981a3-103">ICE99</span></span>

<span data-ttu-id="981a3-104">ICE99 會確認 [目錄](directory-table.md) 資料表中未輸入的屬性名稱會重複保留給 Windows Installer 的公用或私用。</span><span class="sxs-lookup"><span data-stu-id="981a3-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="981a3-105">結果</span><span class="sxs-lookup"><span data-stu-id="981a3-105">Result</span></span>

<span data-ttu-id="981a3-106">ICE99 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="981a3-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="981a3-107">ICE99 錯誤</span><span class="sxs-lookup"><span data-stu-id="981a3-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="981a3-108">Description</span><span class="sxs-lookup"><span data-stu-id="981a3-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="981a3-109">目錄名稱： \[ 1 與 \] 其中一個 MSI 公用屬性相同，而且可能會造成未預期的副作用。</span><span class="sxs-lookup"><span data-stu-id="981a3-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="981a3-110">[目錄](directory-table.md)資料表的目錄資料行中的值會重複 Windows Installer 所保留的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="981a3-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="981a3-111">範例</span><span class="sxs-lookup"><span data-stu-id="981a3-111">Example</span></span>

<span data-ttu-id="981a3-112">ICE99 會報告此範例的下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="981a3-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="981a3-113">[目錄](directory-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="981a3-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="981a3-114">目錄</span><span class="sxs-lookup"><span data-stu-id="981a3-114">Directory</span></span>        | <span data-ttu-id="981a3-115">目錄 \_ 父系</span><span class="sxs-lookup"><span data-stu-id="981a3-115">Directory\_Parent</span></span> | <span data-ttu-id="981a3-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="981a3-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="981a3-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="981a3-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="981a3-118">若要修正此警告，您應該變更 CustomActionData 的名稱。</span><span class="sxs-lookup"><span data-stu-id="981a3-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="981a3-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="981a3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="981a3-120">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="981a3-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="981a3-121">目錄資料表</span><span class="sxs-lookup"><span data-stu-id="981a3-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="981a3-122">Windows Installer 3.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="981a3-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



