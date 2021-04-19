---
description: 指定傳送 EAPOL-Start 訊息的數目上限。
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: maxStart (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983611"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="3fcdc-103">maxStart (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="3fcdc-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="3fcdc-104">MaxStart (OneX) 元素會指定傳送的 EAPOL-Start 訊息數目上限。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="3fcdc-105">在傳送 EAPOL-Start 訊息的數目上限之後，用戶端會假設網路上沒有任何驗證器存在。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="3fcdc-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-106">This element is optional.</span></span> <span data-ttu-id="3fcdc-107">當設定檔中未指定 maxStart 時，會使用3個訊息的值。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="3fcdc-108">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="3fcdc-109">**MaxStart** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="3fcdc-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fcdc-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fcdc-110">Requirements</span></span>



| <span data-ttu-id="3fcdc-111">需求</span><span class="sxs-lookup"><span data-stu-id="3fcdc-111">Requirement</span></span> | <span data-ttu-id="3fcdc-112">值</span><span class="sxs-lookup"><span data-stu-id="3fcdc-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3fcdc-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fcdc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3fcdc-114">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fcdc-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3fcdc-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fcdc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3fcdc-116">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fcdc-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fcdc-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fcdc-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fcdc-118">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3fcdc-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3fcdc-119">**OneX**</span><span class="sxs-lookup"><span data-stu-id="3fcdc-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="3fcdc-120">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3fcdc-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3fcdc-121">**OneX**</span><span class="sxs-lookup"><span data-stu-id="3fcdc-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




