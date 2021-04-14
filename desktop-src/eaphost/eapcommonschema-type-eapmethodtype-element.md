---
title: 輸入 (EapMethodType) 元素
description: 瞭解 (EapMethodType) 元素類型，這是指 EAP 方法類型。 查看需求並查看其他可用的資源。
ms.assetid: 7911e97c-9436-4d60-8497-bee45cdb8db4
keywords:
- Type 元素 EAPHost
topic_type:
- apiref
api_name:
- Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d45defd098f560d4deb8698e0fd569492668e0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382865"
---
# <a name="type-eapmethodtype-element"></a><span data-ttu-id="0ef3e-105">輸入 (EapMethodType) 元素</span><span class="sxs-lookup"><span data-stu-id="0ef3e-105">Type (EapMethodType) Element</span></span>

<span data-ttu-id="0ef3e-106">**類型 (EapMethodType)** 元素會參考 EAP 方法類型。</span><span class="sxs-lookup"><span data-stu-id="0ef3e-106">The **Type (EapMethodType)** element refers to the EAP method type.</span></span>

<span data-ttu-id="0ef3e-107">此類型是由網際網路指派的號碼授權單位所發出的唯一號碼 (IANA) 。</span><span class="sxs-lookup"><span data-stu-id="0ef3e-107">The Type is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="Type"
    type="unsignedByte"
 />
```

<span data-ttu-id="0ef3e-108">**Type** 元素是由 [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="0ef3e-108">The **Type** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef3e-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ef3e-109">Requirements</span></span>



| <span data-ttu-id="0ef3e-110">角色</span><span class="sxs-lookup"><span data-stu-id="0ef3e-110">Role</span></span> | <span data-ttu-id="0ef3e-111">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="0ef3e-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="0ef3e-112">用戶端</span><span class="sxs-lookup"><span data-stu-id="0ef3e-112">Client</span></span><br/> | <span data-ttu-id="0ef3e-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ef3e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ef3e-114">伺服器</span><span class="sxs-lookup"><span data-stu-id="0ef3e-114">Server</span></span><br/> | <span data-ttu-id="0ef3e-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ef3e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ef3e-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ef3e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ef3e-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="0ef3e-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0ef3e-118">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="0ef3e-118">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="0ef3e-119">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="0ef3e-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0ef3e-120">eapcommon 架構</span><span class="sxs-lookup"><span data-stu-id="0ef3e-120">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





