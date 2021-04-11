---
description: 指定有線網路的自動設定服務是否會嘗試使用 802.1 X 進行埠驗證。
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: OneXEnabled (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193667"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="2c848-103">OneXEnabled (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="2c848-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="2c848-104">**OneXEnabled** (security) 元素會指定有線網路的自動設定服務是否會嘗試使用 802.1 x 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="2c848-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="2c848-105">當 **OneXEnabled** 為 FALSE 時，自動設定服務永遠不會使用 802.1 x 進行埠驗證。</span><span class="sxs-lookup"><span data-stu-id="2c848-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="2c848-106">當 **OneXEnabled** 為 TRUE 時，自動設定服務會使用 802.1 x 嘗試埠驗證。</span><span class="sxs-lookup"><span data-stu-id="2c848-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="2c848-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="2c848-107">This element is optional.</span></span> <span data-ttu-id="2c848-108">預設值為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="2c848-108">The default value is TRUE.</span></span> <span data-ttu-id="2c848-109">當設定檔中未指定 **OneXEnabled** 時，802.1 x 可能會用於埠驗證。</span><span class="sxs-lookup"><span data-stu-id="2c848-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="2c848-110">**OneXEnabled** 元素是由 [**安全性**](lan-profileschema-security-msm-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="2c848-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c848-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c848-111">Requirements</span></span>



| <span data-ttu-id="2c848-112">需求</span><span class="sxs-lookup"><span data-stu-id="2c848-112">Requirement</span></span> | <span data-ttu-id="2c848-113">值</span><span class="sxs-lookup"><span data-stu-id="2c848-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c848-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c848-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2c848-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c848-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c848-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c848-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2c848-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c848-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c848-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c848-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c848-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="2c848-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2c848-120">**安全**</span><span class="sxs-lookup"><span data-stu-id="2c848-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="2c848-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="2c848-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2c848-122">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="2c848-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




