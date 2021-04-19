---
description: 指出是否加密共用金鑰。
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: protected (sharedKey) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970792"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="f4313-103">protected (sharedKey) 元素</span><span class="sxs-lookup"><span data-stu-id="f4313-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="f4313-104">Protected (sharedKey) 元素會指出共用金鑰是否已加密。</span><span class="sxs-lookup"><span data-stu-id="f4313-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="f4313-105">元素是由 [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="f4313-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4313-106">備註</span><span class="sxs-lookup"><span data-stu-id="f4313-106">Remarks</span></span>

<span data-ttu-id="f4313-107">若為 Windows Vista 和 Windows Server 2008，如果設定檔是從設定檔存放區取出 (例如，藉由呼叫 [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)) ，則 **受保護** 的永遠會有 TRUE 值。</span><span class="sxs-lookup"><span data-stu-id="f4313-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="f4313-108">適用于 Windows XP Service Pack 3 的設定檔 (SP3) 或適用于 Windows XP Service Pack 2 (SP2) 的無線區域網路 API， **受保護** 的值必須為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="f4313-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="f4313-109">範例</span><span class="sxs-lookup"><span data-stu-id="f4313-109">Examples</span></span>

<span data-ttu-id="f4313-110">若要使用 **受保護** 的元素來查看範例設定檔，請參閱 [無線設定檔範例](wireless-profile-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="f4313-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4313-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4313-111">Requirements</span></span>



| <span data-ttu-id="f4313-112">需求</span><span class="sxs-lookup"><span data-stu-id="f4313-112">Requirement</span></span> | <span data-ttu-id="f4313-113">值</span><span class="sxs-lookup"><span data-stu-id="f4313-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f4313-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4313-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f4313-115">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4313-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4313-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4313-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f4313-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4313-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f4313-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f4313-118">Redistributable</span></span><br/>          | <span data-ttu-id="f4313-119">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="f4313-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f4313-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4313-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4313-121">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="f4313-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f4313-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="f4313-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="f4313-123">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="f4313-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f4313-124">**sharedKey (安全性)**</span><span class="sxs-lookup"><span data-stu-id="f4313-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




