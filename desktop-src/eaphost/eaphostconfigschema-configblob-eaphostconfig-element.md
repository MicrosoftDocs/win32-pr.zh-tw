---
title: ConfigBlob (EapHostConfig) 元素
description: 當方法設定為二進位 BLOB 格式，而不是文字字串格式時，就會使用。
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- ConfigBlob 元素 EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685456"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="b2690-104">ConfigBlob (EapHostConfig) 元素</span><span class="sxs-lookup"><span data-stu-id="b2690-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="b2690-105">當方法設定為二進位 BLOB 格式，而不是文字字串格式時，就會使用 **ConfigBlob (EapHostConfig)** 元素。</span><span class="sxs-lookup"><span data-stu-id="b2690-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="b2690-106">**ConfigBlob** 元素是由 [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b2690-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2690-107">備註</span><span class="sxs-lookup"><span data-stu-id="b2690-107">Remarks</span></span>

<span data-ttu-id="b2690-108">無法同時使用 [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) 和 **ConfigBlob** 元素。</span><span class="sxs-lookup"><span data-stu-id="b2690-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2690-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2690-109">Requirements</span></span>



| <span data-ttu-id="b2690-110">需求</span><span class="sxs-lookup"><span data-stu-id="b2690-110">Requirement</span></span> | <span data-ttu-id="b2690-111">值</span><span class="sxs-lookup"><span data-stu-id="b2690-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b2690-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2690-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b2690-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2690-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b2690-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2690-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b2690-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2690-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2690-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2690-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2690-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b2690-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b2690-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="b2690-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="b2690-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b2690-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b2690-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="b2690-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="b2690-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b2690-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b2690-122">eaphostconfig 架構</span><span class="sxs-lookup"><span data-stu-id="b2690-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





