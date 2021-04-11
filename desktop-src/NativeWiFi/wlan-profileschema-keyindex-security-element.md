---
description: 指定應該使用哪一個金鑰索引來加密無線流量。 只有當 keyType 設定為 &\# 0034; networkKey&0034; 時，才會使用此值 \# 。
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: 索引鍵索引 (安全性) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115821"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="1e5a0-104">索引鍵索引 (安全性) 元素</span><span class="sxs-lookup"><span data-stu-id="1e5a0-104">keyIndex (security) Element</span></span>

<span data-ttu-id="1e5a0-105">索引鍵索引 (security) 元素會指定應該使用哪一個金鑰索引來加密無線流量。</span><span class="sxs-lookup"><span data-stu-id="1e5a0-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="1e5a0-106">只有當 [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) 設定為 "networkKey" 時，才會使用這個。</span><span class="sxs-lookup"><span data-stu-id="1e5a0-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="1e5a0-107">元素是由 [**安全性**](wlan-profileschema-security-msm-element.md) 元素所定義。</span><span class="sxs-lookup"><span data-stu-id="1e5a0-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5a0-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e5a0-108">Requirements</span></span>



| <span data-ttu-id="1e5a0-109">需求</span><span class="sxs-lookup"><span data-stu-id="1e5a0-109">Requirement</span></span> | <span data-ttu-id="1e5a0-110">值</span><span class="sxs-lookup"><span data-stu-id="1e5a0-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1e5a0-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e5a0-111">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5a0-112">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5a0-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1e5a0-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e5a0-113">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5a0-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e5a0-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1e5a0-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1e5a0-115">Redistributable</span></span><br/>          | <span data-ttu-id="1e5a0-116">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="1e5a0-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1e5a0-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e5a0-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="1e5a0-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1e5a0-119">**安全**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="1e5a0-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1e5a0-121">**(MSM) 的安全性**</span><span class="sxs-lookup"><span data-stu-id="1e5a0-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




