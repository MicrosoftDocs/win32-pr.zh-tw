---
title: BaseEapMethodConfig 複雜類型
description: 瞭解 BaseEapMethodConfig 複雜類型。 此類型是方法設定的預留位置元素。
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig 複雜類型 EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382894"
---
# <a name="baseeapmethodconfig-complex-type"></a><span data-ttu-id="91ef7-105">BaseEapMethodConfig 複雜類型</span><span class="sxs-lookup"><span data-stu-id="91ef7-105">BaseEapMethodConfig Complex Type</span></span>

<span data-ttu-id="91ef7-106">**BaseEapMethodConfig** 複雜型別是方法設定的預留位置元素。</span><span class="sxs-lookup"><span data-stu-id="91ef7-106">The **BaseEapMethodConfig** complex type is a placeholder element for the method configuration.</span></span>

``` syntax
<xs:complexType name="BaseEapMethodConfig">
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

## <a name="remarks"></a><span data-ttu-id="91ef7-107">備註</span><span class="sxs-lookup"><span data-stu-id="91ef7-107">Remarks</span></span>

<span data-ttu-id="91ef7-108">EAP 方法會在 **BaseEapMethodConfig** 元素的內容上執行架構驗證。</span><span class="sxs-lookup"><span data-stu-id="91ef7-108">The EAP method performs schema validation on the contents of the **BaseEapMethodConfig** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ef7-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="91ef7-109">Requirements</span></span>



| <span data-ttu-id="91ef7-110">角色</span><span class="sxs-lookup"><span data-stu-id="91ef7-110">Role</span></span> | <span data-ttu-id="91ef7-111">最低支援作業系統版本</span><span class="sxs-lookup"><span data-stu-id="91ef7-111">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="91ef7-112">用戶端</span><span class="sxs-lookup"><span data-stu-id="91ef7-112">Client</span></span><br/> | <span data-ttu-id="91ef7-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91ef7-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91ef7-114">伺服器</span><span class="sxs-lookup"><span data-stu-id="91ef7-114">Server</span></span><br/> | <span data-ttu-id="91ef7-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91ef7-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91ef7-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91ef7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ef7-117">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="91ef7-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="91ef7-118">baseeapmethodconfig 架構</span><span class="sxs-lookup"><span data-stu-id="91ef7-118">baseeapmethodconfig Schema</span></span>](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





