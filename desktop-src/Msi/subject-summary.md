---
description: '[主旨摘要] 屬性的值會傳達封裝所安裝之產品、轉換或修補程式的名稱。'
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: 主體摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993313"
---
# <a name="subject-summary-property"></a><span data-ttu-id="731f5-103">主體摘要屬性</span><span class="sxs-lookup"><span data-stu-id="731f5-103">Subject Summary property</span></span>

<span data-ttu-id="731f5-104">[主旨 **摘要** ] 屬性的值會傳達封裝所安裝之產品、轉換或修補程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="731f5-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="731f5-105">它是由安裝資料庫、轉換或修補套件的作者所組成，以提供摘要資訊中這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="731f5-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="731f5-106">作者應該執行下列動作，以判斷正確的值。</span><span class="sxs-lookup"><span data-stu-id="731f5-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="731f5-107">將安裝套件中的 [主旨 **摘要** ] 屬性設定為與 [**ProductName**](productname.md) 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="731f5-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="731f5-108">將轉換中的 [主旨 **摘要** ] 屬性設定為與原始安裝套件中的 [主旨 **摘要** ] 屬性相同的值。</span><span class="sxs-lookup"><span data-stu-id="731f5-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="731f5-109">在 patch 封裝的摘要資訊中，將 [主旨 **摘要** ] 屬性設定為包含產品名稱之修補程式的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="731f5-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="731f5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="731f5-110">Requirements</span></span>



| <span data-ttu-id="731f5-111">需求</span><span class="sxs-lookup"><span data-stu-id="731f5-111">Requirement</span></span> | <span data-ttu-id="731f5-112">值</span><span class="sxs-lookup"><span data-stu-id="731f5-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731f5-113">版本</span><span class="sxs-lookup"><span data-stu-id="731f5-113">Version</span></span><br/> | <span data-ttu-id="731f5-114">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="731f5-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="731f5-115">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="731f5-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="731f5-116">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="731f5-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="731f5-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="731f5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731f5-118">**PATCHNEWSUMMARYSUBJECT**</span><span class="sxs-lookup"><span data-stu-id="731f5-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="731f5-119">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="731f5-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




