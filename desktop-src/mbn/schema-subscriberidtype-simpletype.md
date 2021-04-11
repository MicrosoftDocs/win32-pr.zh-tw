---
description: 定義行動寬頻設定檔之 SubscriberID 元素的類型。
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: subscriberIdType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026195"
---
# <a name="subscriberidtype-simple-type"></a><span data-ttu-id="2d448-103">subscriberIdType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="2d448-103">subscriberIdType Simple Type</span></span>

<span data-ttu-id="2d448-104">**SubscriberIdType** 簡單類型會定義行動寬頻設定檔的 [**SubscriberID**](schema-subscriberid-mbnprofile-element.md)元素類型。</span><span class="sxs-lookup"><span data-stu-id="2d448-104">The **subscriberIdType** simple type defines a type for the [**SubscriberID**](schema-subscriberid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="2d448-105">此類型是一或多個字元的集合。</span><span class="sxs-lookup"><span data-stu-id="2d448-105">This type is a collection of one or more characters.</span></span>

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="2d448-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d448-106">Requirements</span></span>



| <span data-ttu-id="2d448-107">需求</span><span class="sxs-lookup"><span data-stu-id="2d448-107">Requirement</span></span> | <span data-ttu-id="2d448-108">值</span><span class="sxs-lookup"><span data-stu-id="2d448-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2d448-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d448-109">Minimum supported client</span></span><br/> | <span data-ttu-id="2d448-110">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d448-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2d448-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d448-111">Minimum supported server</span></span><br/> | <span data-ttu-id="2d448-112">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d448-112">None supported</span></span><br/>                         |



 

 




