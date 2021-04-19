---
description: 中繼限定詞會藉由在 MOF 語法中明確地定義類別或屬性宣告的實際使用方式，來精簡 CIM 模型中中繼結構的定義。
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: 中繼限定詞
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984593"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="ebbc3-103">中繼限定詞</span><span class="sxs-lookup"><span data-stu-id="ebbc3-103">Meta Qualifiers</span></span>

<span data-ttu-id="ebbc3-104">中繼限定詞會藉由在 MOF 語法中明確地定義類別或屬性宣告的實際使用方式，來精簡 CIM 模型中中繼結構的定義。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="ebbc3-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**協會**</span><span class="sxs-lookup"><span data-stu-id="ebbc3-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="ebbc3-106">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ebbc3-106">Data type: **boolean**</span></span>

<span data-ttu-id="ebbc3-107">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="ebbc3-107">Applies to: classes</span></span>

<span data-ttu-id="ebbc3-108">指出類別是否為關聯類別，用來描述兩個其他類別之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="ebbc3-109">缺少這個辨識符號表示類別不是關聯類別。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="ebbc3-110">此辨識符號與 **指示** 互斥。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="ebbc3-111">如需詳細資訊，請參閱宣告 [關聯類別](declaring-an-association-class.md)。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebbc3-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**指示**</span><span class="sxs-lookup"><span data-stu-id="ebbc3-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="ebbc3-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="ebbc3-113">Data type: **boolean**</span></span>

<span data-ttu-id="ebbc3-114">適用于：類別</span><span class="sxs-lookup"><span data-stu-id="ebbc3-114">Applies to: classes</span></span>

<span data-ttu-id="ebbc3-115">指出物件類別是否會定義指示。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="ebbc3-116">此辨識符號與 **關聯** 互斥。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="ebbc3-117">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ebbc3-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebbc3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebbc3-118">Requirements</span></span>



| <span data-ttu-id="ebbc3-119">需求</span><span class="sxs-lookup"><span data-stu-id="ebbc3-119">Requirement</span></span> | <span data-ttu-id="ebbc3-120">值</span><span class="sxs-lookup"><span data-stu-id="ebbc3-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ebbc3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebbc3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbc3-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebbc3-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ebbc3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebbc3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbc3-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebbc3-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebbc3-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebbc3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbc3-126">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="ebbc3-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="ebbc3-127">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="ebbc3-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




