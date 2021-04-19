---
description: 指定要用於啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: AuthProtocol (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977015"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="e1177-103">AuthProtocol (coNtextType) 元素</span><span class="sxs-lookup"><span data-stu-id="e1177-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="e1177-104">**AuthProtocol (coNtextType)** 元素會指定用來啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e1177-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="e1177-105">元素可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e1177-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="e1177-106">值</span><span class="sxs-lookup"><span data-stu-id="e1177-106">Value</span></span>      | <span data-ttu-id="e1177-107">意義</span><span class="sxs-lookup"><span data-stu-id="e1177-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="e1177-108">以上</span><span class="sxs-lookup"><span data-stu-id="e1177-108">"NONE"</span></span>     | <span data-ttu-id="e1177-109">無驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="e1177-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="e1177-110">PAP</span><span class="sxs-lookup"><span data-stu-id="e1177-110">"PAP"</span></span>      | <span data-ttu-id="e1177-111">未加密的密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="e1177-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="e1177-112">CHAP</span><span class="sxs-lookup"><span data-stu-id="e1177-112">"CHAP"</span></span>     | <span data-ttu-id="e1177-113">挑戰交握驗證通訊協定 (CHAP) 。</span><span class="sxs-lookup"><span data-stu-id="e1177-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="e1177-114">Eap-mschapv2</span><span class="sxs-lookup"><span data-stu-id="e1177-114">MsCHAPV2"</span></span> | <span data-ttu-id="e1177-115">使用 Microsoft s 挑戰交握驗證通訊協定 (CHAP) 2.0 版。</span><span class="sxs-lookup"><span data-stu-id="e1177-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="e1177-116">這個元素是選擇性的，且僅供 GSM 設定檔使用。</span><span class="sxs-lookup"><span data-stu-id="e1177-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="e1177-117">如果未指定專案，而且設定檔適用于 GSM 裝置，則行動寬頻服務將使用「 **無**」。</span><span class="sxs-lookup"><span data-stu-id="e1177-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="e1177-118">**AuthProtocol** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="e1177-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1177-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1177-119">Requirements</span></span>



| <span data-ttu-id="e1177-120">需求</span><span class="sxs-lookup"><span data-stu-id="e1177-120">Requirement</span></span> | <span data-ttu-id="e1177-121">值</span><span class="sxs-lookup"><span data-stu-id="e1177-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="e1177-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1177-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e1177-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1177-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e1177-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1177-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e1177-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="e1177-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e1177-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1177-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e1177-127">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="e1177-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e1177-128">**coNtextType**</span><span class="sxs-lookup"><span data-stu-id="e1177-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="e1177-129">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="e1177-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e1177-130">**MBNProfile) 內容 (**</span><span class="sxs-lookup"><span data-stu-id="e1177-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




