---
description: 定義封鎖的網路。
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: network (封鎖清單) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988425"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="a8ddb-103">network (封鎖清單) 元素</span><span class="sxs-lookup"><span data-stu-id="a8ddb-103">network (blockList) Element</span></span>

<span data-ttu-id="a8ddb-104">Network (封鎖清單) 元素會定義封鎖的網路。</span><span class="sxs-lookup"><span data-stu-id="a8ddb-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="a8ddb-105">電腦無法連線到封鎖的網路。</span><span class="sxs-lookup"><span data-stu-id="a8ddb-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="a8ddb-106">**Network** 元素是由 [**封鎖清單**](wlan-policyschema-blocklist-networkfilter-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="a8ddb-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ddb-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8ddb-107">Requirements</span></span>



| <span data-ttu-id="a8ddb-108">需求</span><span class="sxs-lookup"><span data-stu-id="a8ddb-108">Requirement</span></span> | <span data-ttu-id="a8ddb-109">值</span><span class="sxs-lookup"><span data-stu-id="a8ddb-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8ddb-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8ddb-110">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ddb-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8ddb-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8ddb-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8ddb-112">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ddb-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8ddb-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8ddb-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8ddb-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8ddb-115">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="a8ddb-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8ddb-116">**封鎖清單**</span><span class="sxs-lookup"><span data-stu-id="a8ddb-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="a8ddb-117">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="a8ddb-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8ddb-118">**封鎖清單 (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="a8ddb-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




