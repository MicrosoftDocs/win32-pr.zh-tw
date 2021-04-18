---
description: 識別設定檔的唯一識別碼。
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: SubscriberID (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511740"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="66ff1-103">SubscriberID (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="66ff1-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="66ff1-104">**SubscriberID (MBNProfile)** 元素會識別設定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="66ff1-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="66ff1-105">若為 GSM 網路，這應該包含 SIM 的 IMSI (國際行動使用者身分識別) ，而針對 CDMA 裝置，則應該包含裝置的最小 (行動電話識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="66ff1-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="66ff1-106">元素是最大長度為15位數的數值字串。</span><span class="sxs-lookup"><span data-stu-id="66ff1-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="66ff1-107">需要元素。</span><span class="sxs-lookup"><span data-stu-id="66ff1-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="66ff1-108">**SubscriberID** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="66ff1-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ff1-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="66ff1-109">Requirements</span></span>



| <span data-ttu-id="66ff1-110">需求</span><span class="sxs-lookup"><span data-stu-id="66ff1-110">Requirement</span></span> | <span data-ttu-id="66ff1-111">值</span><span class="sxs-lookup"><span data-stu-id="66ff1-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="66ff1-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66ff1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="66ff1-113">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66ff1-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="66ff1-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66ff1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="66ff1-115">都不支援</span><span class="sxs-lookup"><span data-stu-id="66ff1-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="66ff1-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66ff1-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="66ff1-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="66ff1-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="66ff1-118">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="66ff1-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="66ff1-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="66ff1-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="66ff1-120">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="66ff1-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




