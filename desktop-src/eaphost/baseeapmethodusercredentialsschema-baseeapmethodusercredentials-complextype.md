---
title: BaseEapMethodUserCredentials 複雜類型
description: 瞭解 BaseEapMethodUserCredentials 複雜類型。 此類型是方法認證資料的預留位置元素。
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- BaseEapMethodUserCredentials 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37bc7a91a5d90cde6cba1af12bb0a4784ee21c7f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683077"
---
# <a name="baseeapmethodusercredentials-complex-type"></a><span data-ttu-id="f4a2c-105">BaseEapMethodUserCredentials 複雜類型</span><span class="sxs-lookup"><span data-stu-id="f4a2c-105">BaseEapMethodUserCredentials Complex Type</span></span>

<span data-ttu-id="f4a2c-106">**BaseEapMethodUserCredentials** 複雜型別是方法認證資料的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="f4a2c-106">The **BaseEapMethodUserCredentials** complex type is a placeholder element for method credential data.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a><span data-ttu-id="f4a2c-107">備註</span><span class="sxs-lookup"><span data-stu-id="f4a2c-107">Remarks</span></span>

<span data-ttu-id="f4a2c-108">EAP 方法會執行 **BaseEapMethodUserCredentials** 內容的架構驗證。</span><span class="sxs-lookup"><span data-stu-id="f4a2c-108">The EAP method performs schema validation on the contents of **BaseEapMethodUserCredentials**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a2c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4a2c-109">Requirements</span></span>



| <span data-ttu-id="f4a2c-110">角色</span><span class="sxs-lookup"><span data-stu-id="f4a2c-110">Role</span></span> | <span data-ttu-id="f4a2c-111">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="f4a2c-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f4a2c-112">用戶端</span><span class="sxs-lookup"><span data-stu-id="f4a2c-112">Client</span></span><br/> | <span data-ttu-id="f4a2c-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a2c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4a2c-114">伺服器</span><span class="sxs-lookup"><span data-stu-id="f4a2c-114">Server</span></span><br/> | <span data-ttu-id="f4a2c-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a2c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4a2c-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4a2c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a2c-117">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="f4a2c-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f4a2c-118">baseeapmethodusercredentials 架構</span><span class="sxs-lookup"><span data-stu-id="f4a2c-118">baseeapmethodusercredentials Schema</span></span>](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





