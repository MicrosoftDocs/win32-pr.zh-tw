---
title: 層級 (MetadataType) 元素
description: 定義指定事件嚴重性的層級清單。 |層級 (MetadataType) 元素
ms.assetid: 710a4c7e-d37e-4543-8fdf-44688085b996
keywords:
- 層級元素 EventLog
topic_type:
- apiref
api_name:
- levels
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9df4a7d7fc58f21ab6c5c6965b635f8bd087d890
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322327"
---
# <a name="levels-metadatatype-element"></a><span data-ttu-id="f1041-105">層級 (MetadataType) 元素</span><span class="sxs-lookup"><span data-stu-id="f1041-105">levels (MetadataType) Element</span></span>

<span data-ttu-id="f1041-106">定義指定事件嚴重性的層級清單。</span><span class="sxs-lookup"><span data-stu-id="f1041-106">Defines a list of levels that specify the severity of an event.</span></span>

``` syntax
<xs:element name="levels"
    type="LevelListType"
 />
```

<span data-ttu-id="f1041-107">**層級** 元素是由 [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f1041-107">The **levels** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1041-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1041-108">Requirements</span></span>



| <span data-ttu-id="f1041-109">需求</span><span class="sxs-lookup"><span data-stu-id="f1041-109">Requirement</span></span> | <span data-ttu-id="f1041-110">值</span><span class="sxs-lookup"><span data-stu-id="f1041-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1041-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1041-111">Minimum supported client</span></span><br/> | <span data-ttu-id="f1041-112">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1041-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1041-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1041-113">Minimum supported server</span></span><br/> | <span data-ttu-id="f1041-114">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1041-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1041-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1041-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1041-116">**父元素**</span><span class="sxs-lookup"><span data-stu-id="f1041-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="f1041-117">**中繼資料 (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="f1041-117">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





