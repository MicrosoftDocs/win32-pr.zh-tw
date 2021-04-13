---
title: Config (EapHostConfig) 元素
description: 當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用。
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Config 元素 EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465609"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="b9b6a-104">Config (EapHostConfig) 元素</span><span class="sxs-lookup"><span data-stu-id="b9b6a-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="b9b6a-105">當方法設定為 XML 文字格式，而非二進位 BLOB 時，會使用 **Config (EapHostConfig)** 元素。</span><span class="sxs-lookup"><span data-stu-id="b9b6a-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="b9b6a-106">**Config** 元素是由 [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="b9b6a-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9b6a-107">備註</span><span class="sxs-lookup"><span data-stu-id="b9b6a-107">Remarks</span></span>

<span data-ttu-id="b9b6a-108">無法同時使用 **Config** 和 [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="b9b6a-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b6a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9b6a-109">Requirements</span></span>



| <span data-ttu-id="b9b6a-110">需求</span><span class="sxs-lookup"><span data-stu-id="b9b6a-110">Requirement</span></span> | <span data-ttu-id="b9b6a-111">值</span><span class="sxs-lookup"><span data-stu-id="b9b6a-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9b6a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9b6a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b9b6a-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9b6a-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b9b6a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9b6a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b9b6a-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9b6a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9b6a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9b6a-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9b6a-117">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="b9b6a-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b9b6a-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="b9b6a-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="b9b6a-119">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="b9b6a-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b9b6a-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="b9b6a-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="b9b6a-121">EAPHost 和舊版架構</span><span class="sxs-lookup"><span data-stu-id="b9b6a-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b9b6a-122">eaphostconfig 架構</span><span class="sxs-lookup"><span data-stu-id="b9b6a-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





