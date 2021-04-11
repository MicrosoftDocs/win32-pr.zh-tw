---
description: 動態辨識符號表示以動態方式建立實例的類別。 此限定詞的值必須設定為 TRUE。
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: 動態限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848743"
---
# <a name="dynamic-qualifier"></a><span data-ttu-id="9c386-104">動態限定詞</span><span class="sxs-lookup"><span data-stu-id="9c386-104">Dynamic Qualifier</span></span>

<span data-ttu-id="9c386-105">**動態** 辨識符號表示以動態方式建立實例的類別。</span><span class="sxs-lookup"><span data-stu-id="9c386-105">The **Dynamic** qualifier indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="9c386-106">此限定詞的值必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="9c386-106">The value of this qualifier must be set to **TRUE**.</span></span>

<span data-ttu-id="9c386-107">您必須在所有包含資料的類別，以及動態建立的實例上指定 **動態** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="9c386-107">The **Dynamic** qualifier must be specified on all classes that contain data and for which instances are created dynamically.</span></span> <span data-ttu-id="9c386-108">通常也會指定 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號，以識別負責提供資料的提供者。</span><span class="sxs-lookup"><span data-stu-id="9c386-108">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is typically also specified to identify the provider responsible for supplying the data.</span></span>

<span data-ttu-id="9c386-109">只包含需要執行之方法的類別不需要 **動態** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="9c386-109">Classes that contain only methods that need implementation do not require the **Dynamic** qualifier.</span></span> <span data-ttu-id="9c386-110">只有 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號需要指定提供者的名稱，才能提供執行。</span><span class="sxs-lookup"><span data-stu-id="9c386-110">Only the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is required to specify the name of the provider to supply the implementation.</span></span>

<span data-ttu-id="9c386-111">所有衍生自動態類別的類別都必須是動態的。</span><span class="sxs-lookup"><span data-stu-id="9c386-111">All classes derived from a dynamic class must be dynamic.</span></span> <span data-ttu-id="9c386-112">您無法從動態類別衍生靜態類別。</span><span class="sxs-lookup"><span data-stu-id="9c386-112">You cannot derive a static class from a dynamic class.</span></span>

<span data-ttu-id="9c386-113">當在實例的屬性上指定 **動態** 時，也必須指定 **PropertyCoNtext** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="9c386-113">When **Dynamic** is specified on a property of an instance, the **PropertyContext** qualifier must also be specified.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c386-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c386-114">Requirements</span></span>



| <span data-ttu-id="9c386-115">需求</span><span class="sxs-lookup"><span data-stu-id="9c386-115">Requirement</span></span> | <span data-ttu-id="9c386-116">值</span><span class="sxs-lookup"><span data-stu-id="9c386-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9c386-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c386-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c386-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c386-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9c386-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c386-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c386-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c386-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c386-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c386-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c386-122">**標準 WMI 限定詞**</span><span class="sxs-lookup"><span data-stu-id="9c386-122">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="9c386-123">WMI 限定詞</span><span class="sxs-lookup"><span data-stu-id="9c386-123">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="9c386-124">新增限定詞</span><span class="sxs-lookup"><span data-stu-id="9c386-124">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




