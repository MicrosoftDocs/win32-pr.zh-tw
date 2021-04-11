---
description: 指定要用於行動寬頻裝置的自動連線設定。
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943405"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="69128-103">ConnectionMode (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="69128-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="69128-104">**ConnectionMode (MBNProfile)** 元素會指定要用於行動寬頻裝置的自動連線設定。</span><span class="sxs-lookup"><span data-stu-id="69128-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="69128-105">這個元素可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="69128-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="69128-106">值</span><span class="sxs-lookup"><span data-stu-id="69128-106">Value</span></span>       | <span data-ttu-id="69128-107">意義</span><span class="sxs-lookup"><span data-stu-id="69128-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="69128-108">》</span><span class="sxs-lookup"><span data-stu-id="69128-108">"manual"</span></span>    | <span data-ttu-id="69128-109">永遠不會自動連接到網路。</span><span class="sxs-lookup"><span data-stu-id="69128-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="69128-110">auto</span><span class="sxs-lookup"><span data-stu-id="69128-110">"auto"</span></span>      | <span data-ttu-id="69128-111">一律自動連接到網路。</span><span class="sxs-lookup"><span data-stu-id="69128-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="69128-112">「自動首頁」</span><span class="sxs-lookup"><span data-stu-id="69128-112">"auto-home"</span></span> | <span data-ttu-id="69128-113">會自動連接到網路，但在漫遊網路中的情況除外。</span><span class="sxs-lookup"><span data-stu-id="69128-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="69128-114">此元素最多可有一次。</span><span class="sxs-lookup"><span data-stu-id="69128-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="69128-115">此為必要項目。</span><span class="sxs-lookup"><span data-stu-id="69128-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="69128-116">**ConnectionMode** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="69128-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="69128-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="69128-117">Requirements</span></span>



| <span data-ttu-id="69128-118">需求</span><span class="sxs-lookup"><span data-stu-id="69128-118">Requirement</span></span> | <span data-ttu-id="69128-119">值</span><span class="sxs-lookup"><span data-stu-id="69128-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="69128-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69128-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69128-121">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69128-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="69128-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69128-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69128-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="69128-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="69128-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69128-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="69128-125">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="69128-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="69128-126">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="69128-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="69128-127">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="69128-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="69128-128">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="69128-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




