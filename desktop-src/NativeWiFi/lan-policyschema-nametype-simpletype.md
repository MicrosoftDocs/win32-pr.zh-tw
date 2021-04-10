---
description: 針對有線區域網路原則設定檔的名稱或描述定義字串類型。
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
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
ms.openlocfilehash: 702ee6340fa3d03217c884a48625d3a38be4ad9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944641"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="fb1fa-103">nameType 簡單類型 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="fb1fa-103">nameType simple type (LAN_policy)</span></span>

<span data-ttu-id="fb1fa-104">NameType 簡單類型會針對有線區域網路原則設定檔的名稱或描述定義字串類型。</span><span class="sxs-lookup"><span data-stu-id="fb1fa-104">The nameType simple type defines a string type for either the name or the description of a wired LAN policy profile.</span></span> <span data-ttu-id="fb1fa-105">名稱和描述是長度至少為1個字元且長度最多為255個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="fb1fa-105">Names and descriptions are strings that are at least one character long and at most 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="fb1fa-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb1fa-106">Requirements</span></span>



| <span data-ttu-id="fb1fa-107">需求</span><span class="sxs-lookup"><span data-stu-id="fb1fa-107">Requirement</span></span> | <span data-ttu-id="fb1fa-108">值</span><span class="sxs-lookup"><span data-stu-id="fb1fa-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb1fa-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb1fa-109">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1fa-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb1fa-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb1fa-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb1fa-111">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1fa-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb1fa-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




