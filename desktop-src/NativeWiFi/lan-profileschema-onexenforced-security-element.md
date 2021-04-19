---
description: 指定有線網路的自動設定服務是否需要使用 802.1 X 進行埠驗證。
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: OneXEnforced (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990332"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="e6e21-103">OneXEnforced (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="e6e21-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="e6e21-104">**OneXEnforced** (security) 元素會指定有線網路的自動設定服務是否需要使用 802.1 x 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="e6e21-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="e6e21-105">當 **OneXEnforced** 為 TRUE 時，自動設定服務必須使用 802.1 x 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="e6e21-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="e6e21-106">當 **OneXEnforced** 為 FALSE 時，自動設定服務會嘗試使用 802.1 x 進行埠驗證，但如果 802.1 x 驗證因任何原因而失敗，則此服務會回復為無驗證。</span><span class="sxs-lookup"><span data-stu-id="e6e21-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="e6e21-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="e6e21-107">This element is optional.</span></span> <span data-ttu-id="e6e21-108">預設值為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="e6e21-108">The default value is FALSE.</span></span>

<span data-ttu-id="e6e21-109">如果 [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) 為 TRUE，則這個元素只有一個有意義的值。</span><span class="sxs-lookup"><span data-stu-id="e6e21-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="e6e21-110">如果 **OneXEnabled** 為 FALSE，則會忽略此元素的值。</span><span class="sxs-lookup"><span data-stu-id="e6e21-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="e6e21-111">**OneXEnforced** 元素是由 [**安全性**](lan-profileschema-security-msm-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="e6e21-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e21-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6e21-112">Requirements</span></span>



| <span data-ttu-id="e6e21-113">需求</span><span class="sxs-lookup"><span data-stu-id="e6e21-113">Requirement</span></span> | <span data-ttu-id="e6e21-114">值</span><span class="sxs-lookup"><span data-stu-id="e6e21-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6e21-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6e21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e21-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6e21-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6e21-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6e21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e21-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6e21-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6e21-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6e21-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6e21-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e6e21-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e6e21-121">**安全**</span><span class="sxs-lookup"><span data-stu-id="e6e21-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="e6e21-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e6e21-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e6e21-123">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="e6e21-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




