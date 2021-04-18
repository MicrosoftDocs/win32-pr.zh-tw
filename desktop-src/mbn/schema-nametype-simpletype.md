---
description: 定義 Mobile 寬頻設定檔的字串類型。
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: 'nameType 簡單類型 (行動寬頻) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971237"
---
# <a name="nametype-simple-type-mobile-broadband"></a><span data-ttu-id="87c27-103">nameType 簡單類型 (行動寬頻) </span><span class="sxs-lookup"><span data-stu-id="87c27-103">nameType simple type (Mobile Broadband)</span></span>

<span data-ttu-id="87c27-104">**NameType** simple type 會定義 Mobile 寬頻設定檔的字串類型。</span><span class="sxs-lookup"><span data-stu-id="87c27-104">The **nameType** simple type defines a string type for the Mobile Broadband profile.</span></span> <span data-ttu-id="87c27-105">這個字串的長度至少要有一個字元，且長度最多為255個字元。</span><span class="sxs-lookup"><span data-stu-id="87c27-105">This string is at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="87c27-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="87c27-106">Requirements</span></span>



| <span data-ttu-id="87c27-107">需求</span><span class="sxs-lookup"><span data-stu-id="87c27-107">Requirement</span></span> | <span data-ttu-id="87c27-108">值</span><span class="sxs-lookup"><span data-stu-id="87c27-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="87c27-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="87c27-109">Minimum supported client</span></span><br/> | <span data-ttu-id="87c27-110">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="87c27-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="87c27-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="87c27-111">Minimum supported server</span></span><br/> | <span data-ttu-id="87c27-112">都不支援</span><span class="sxs-lookup"><span data-stu-id="87c27-112">None supported</span></span><br/>                         |



 

 




