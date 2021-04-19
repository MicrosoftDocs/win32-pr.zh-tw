---
description: 指出是否使用 802.1 X 驗證。
ms.assetid: dbddaf5a-7574-4282-ab4d-f6f697ed94ab
title: useOneX (authEncryption) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cb327be4006e8da0074815a74e49d3ccdc5d3c84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106969418"
---
# <a name="useonex-authencryption-element"></a><span data-ttu-id="5348e-103">useOneX (authEncryption) 元素</span><span class="sxs-lookup"><span data-stu-id="5348e-103">useOneX (authEncryption) Element</span></span>

<span data-ttu-id="5348e-104">UseOneX (authEncryption) 元素指出是否使用 802.1 X 驗證。</span><span class="sxs-lookup"><span data-stu-id="5348e-104">The useOneX (authEncryption) element indicates whether 802.1X authentication is used.</span></span>

``` syntax
<xs:element name="useOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="5348e-105">元素是由 [**authEncryption**](wlan-profileschema-authencryption-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="5348e-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="5348e-106">範例</span><span class="sxs-lookup"><span data-stu-id="5348e-106">Examples</span></span>

<span data-ttu-id="5348e-107">若要查看使用 **useOneX** 元素的範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="5348e-107">To view sample profiles that use the **useOneX** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5348e-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="5348e-108">Requirements</span></span>



| <span data-ttu-id="5348e-109">需求</span><span class="sxs-lookup"><span data-stu-id="5348e-109">Requirement</span></span> | <span data-ttu-id="5348e-110">值</span><span class="sxs-lookup"><span data-stu-id="5348e-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="5348e-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5348e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="5348e-112">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5348e-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5348e-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5348e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="5348e-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5348e-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="5348e-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5348e-115">Redistributable</span></span><br/>          | <span data-ttu-id="5348e-116">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="5348e-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5348e-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5348e-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="5348e-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="5348e-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5348e-119">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="5348e-119">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="5348e-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="5348e-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5348e-121">**authEncryption (安全性)**</span><span class="sxs-lookup"><span data-stu-id="5348e-121">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




