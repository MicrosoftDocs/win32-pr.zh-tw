---
title: 安全性 (SystemPropertiesType) 元素
description: 識別記錄事件的使用者。
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- 安全性元素 EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105797"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="d361d-104">安全性 (SystemPropertiesType) 元素</span><span class="sxs-lookup"><span data-stu-id="d361d-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="d361d-105">識別記錄事件的使用者。</span><span class="sxs-lookup"><span data-stu-id="d361d-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="d361d-106">**安全性** 元素是由 [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="d361d-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="d361d-107">屬性</span><span class="sxs-lookup"><span data-stu-id="d361d-107">Attributes</span></span>



| <span data-ttu-id="d361d-108">名稱</span><span class="sxs-lookup"><span data-stu-id="d361d-108">Name</span></span>   | <span data-ttu-id="d361d-109">類型</span><span class="sxs-lookup"><span data-stu-id="d361d-109">Type</span></span>   | <span data-ttu-id="d361d-110">Description</span><span class="sxs-lookup"><span data-stu-id="d361d-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="d361d-111">UserID</span><span class="sxs-lookup"><span data-stu-id="d361d-111">UserID</span></span> | <span data-ttu-id="d361d-112">字串</span><span class="sxs-lookup"><span data-stu-id="d361d-112">string</span></span> | <span data-ttu-id="d361d-113">以字串形式 (SID) 使用者的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="d361d-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d361d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d361d-114">Requirements</span></span>



| <span data-ttu-id="d361d-115">需求</span><span class="sxs-lookup"><span data-stu-id="d361d-115">Requirement</span></span> | <span data-ttu-id="d361d-116">值</span><span class="sxs-lookup"><span data-stu-id="d361d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d361d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d361d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d361d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d361d-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d361d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d361d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d361d-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d361d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d361d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d361d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="d361d-122">**父元素**</span><span class="sxs-lookup"><span data-stu-id="d361d-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d361d-123">**系統 (的系統事件)**</span><span class="sxs-lookup"><span data-stu-id="d361d-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





