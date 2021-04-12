---
description: 如果封裝使用條件類型之資料庫資料行中的 AdminUser 屬性，ICE86 會發出警告。 封裝作者應該在條件陳述式中使用具特殊許可權的屬性。
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320084"
---
# <a name="ice86"></a><span data-ttu-id="3be13-104">ICE86</span><span class="sxs-lookup"><span data-stu-id="3be13-104">ICE86</span></span>

<span data-ttu-id="3be13-105">如果封裝使用 [條件](condition.md)類型之資料庫資料行中的 [**ADMINUSER**](adminuser.md)屬性，ICE86 會發出警告。</span><span class="sxs-lookup"><span data-stu-id="3be13-105">ICE86 issues a warning if the package uses the [**AdminUser**](adminuser.md) property in database column of the [Condition](condition.md) type.</span></span> <span data-ttu-id="3be13-106">封裝作者應該在條件陳述式中使用具特殊 [**許可權**](privileged.md) 的屬性。</span><span class="sxs-lookup"><span data-stu-id="3be13-106">Package authors should use the [**Privileged**](privileged.md) property in conditional statements.</span></span>

## <a name="result"></a><span data-ttu-id="3be13-107">結果</span><span class="sxs-lookup"><span data-stu-id="3be13-107">Result</span></span>

<span data-ttu-id="3be13-108">ICE86 會張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="3be13-108">ICE86 posts the following warning.</span></span>



| <span data-ttu-id="3be13-109">ICE86 警告</span><span class="sxs-lookup"><span data-stu-id="3be13-109">ICE86 warning</span></span>                                                                                               | <span data-ttu-id="3be13-110">Description</span><span class="sxs-lookup"><span data-stu-id="3be13-110">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3be13-111">\` \` 在資料行% s 中找到屬性% s \` \` 。 \`% s \` 在資料列% s 中。</span><span class="sxs-lookup"><span data-stu-id="3be13-111">Property \`%s\` found in column \`%s\`.\`%s\` in row %s.</span></span> <span data-ttu-id="3be13-112">\`具有特殊許可權 \` 的屬性通常更適合。</span><span class="sxs-lookup"><span data-stu-id="3be13-112">\`Privileged\` property is often more appropriate.</span></span> | <span data-ttu-id="3be13-113">在條件欄位中使用 [**AdminUser**](adminuser.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="3be13-113">[**AdminUser**](adminuser.md) property was used in a Condition field.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3be13-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="3be13-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be13-115">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="3be13-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



