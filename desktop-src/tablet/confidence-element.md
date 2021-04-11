---
description: 包含 InkWord 的日記本筆墨分析器所傳回的信賴評等。
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: 信賴元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112016"
---
# <a name="confidence-element"></a><span data-ttu-id="3b52d-103">信賴元素</span><span class="sxs-lookup"><span data-stu-id="3b52d-103">Confidence Element</span></span>

<span data-ttu-id="3b52d-104">包含 [**InkWord**](inkword-element.md)的日記本筆墨分析器所傳回的信賴評等。</span><span class="sxs-lookup"><span data-stu-id="3b52d-104">Contains the confidence rating returned by the Journal ink analyzer for the [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="3b52d-105">定義</span><span class="sxs-lookup"><span data-stu-id="3b52d-105">Definition</span></span>

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="3b52d-106">父項目</span><span class="sxs-lookup"><span data-stu-id="3b52d-106">Parent Elements</span></span>

[<span data-ttu-id="3b52d-107">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="3b52d-107">**InkWord**</span></span>](inkword-element.md)

## <a name="values"></a><span data-ttu-id="3b52d-108">值</span><span class="sxs-lookup"><span data-stu-id="3b52d-108">Values</span></span>

<span data-ttu-id="3b52d-109">此欄位的有效值包括 "0"、"1" 和 "2"。</span><span class="sxs-lookup"><span data-stu-id="3b52d-109">Valid values for this field include "0", "1", and "2".</span></span> <span data-ttu-id="3b52d-110">0表示強烈的信賴度，1表示中繼信賴度，2表示不佳的信賴度。</span><span class="sxs-lookup"><span data-stu-id="3b52d-110">0 indicates Strong confidence, 1 indicates Intermediate confidence, and 2 indicates Poor confidence.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3b52d-111">子元素</span><span class="sxs-lookup"><span data-stu-id="3b52d-111">Child Elements</span></span>

<span data-ttu-id="3b52d-112">無。</span><span class="sxs-lookup"><span data-stu-id="3b52d-112">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="3b52d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3b52d-113">Attributes</span></span>

<span data-ttu-id="3b52d-114">無。</span><span class="sxs-lookup"><span data-stu-id="3b52d-114">None.</span></span>

## <a name="element-information"></a><span data-ttu-id="3b52d-115">項目資訊</span><span class="sxs-lookup"><span data-stu-id="3b52d-115">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="3b52d-116">項目類型</span><span class="sxs-lookup"><span data-stu-id="3b52d-116">Element type</span></span> | <span data-ttu-id="3b52d-117">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="3b52d-117">**xs:string**</span></span>                              |
| <span data-ttu-id="3b52d-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b52d-118">Namespace</span></span>    | <span data-ttu-id="3b52d-119">urn：架構-microsoft-com：平板電腦： richink</span><span class="sxs-lookup"><span data-stu-id="3b52d-119">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="3b52d-120">結構描述名稱</span><span class="sxs-lookup"><span data-stu-id="3b52d-120">Schema name</span></span>  | <span data-ttu-id="3b52d-121">日誌讀者</span><span class="sxs-lookup"><span data-stu-id="3b52d-121">Journal Reader</span></span>                             |



 

 

 



