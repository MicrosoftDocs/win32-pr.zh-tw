---
description: 針對無線區域網路原則設定檔的名稱或描述定義字串類型。
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: 'nameType 簡單類型 (LAN_policy) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985361"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="e69a4-103">nameType 簡單類型 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="e69a4-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="e69a4-104">NameType simple type 會針對無線區域網路原則設定檔的名稱或描述定義字串類型。</span><span class="sxs-lookup"><span data-stu-id="e69a4-104">The nameType simple type defines a string type for either the name or the description of a wireless LAN policy profile.</span></span> <span data-ttu-id="e69a4-105">名稱和描述是長度至少為1個字元且長度最多為255個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="e69a4-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
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

## <a name="requirements"></a><span data-ttu-id="e69a4-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="e69a4-106">Requirements</span></span>



| <span data-ttu-id="e69a4-107">需求</span><span class="sxs-lookup"><span data-stu-id="e69a4-107">Requirement</span></span> | <span data-ttu-id="e69a4-108">值</span><span class="sxs-lookup"><span data-stu-id="e69a4-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e69a4-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e69a4-109">Minimum supported client</span></span><br/> | <span data-ttu-id="e69a4-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e69a4-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e69a4-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e69a4-111">Minimum supported server</span></span><br/> | <span data-ttu-id="e69a4-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e69a4-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




