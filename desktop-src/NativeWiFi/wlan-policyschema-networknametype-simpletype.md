---
description: 定義服務組識別元 (Ssid) 的字串類型。
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: networkNameType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6b6463644e1bd174be256d51b34ae2ae4ad9ce07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945052"
---
# <a name="networknametype-simple-type"></a><span data-ttu-id="6fb6d-103">networkNameType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="6fb6d-103">networkNameType Simple Type</span></span>

<span data-ttu-id="6fb6d-104">NetworkNameType 簡單類型會定義服務組識別元 (Ssid) 的字串類型。</span><span class="sxs-lookup"><span data-stu-id="6fb6d-104">The networkNameType simple type defines a string type for service set identifiers (SSIDs).</span></span> <span data-ttu-id="6fb6d-105">SSID 是長度至少為1個字元且長度最多為32個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="6fb6d-105">A SSID is a string that is at least one character long and at most 32 characters long.</span></span>

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="6fb6d-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fb6d-106">Requirements</span></span>



| <span data-ttu-id="6fb6d-107">需求</span><span class="sxs-lookup"><span data-stu-id="6fb6d-107">Requirement</span></span> | <span data-ttu-id="6fb6d-108">值</span><span class="sxs-lookup"><span data-stu-id="6fb6d-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6fb6d-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fb6d-109">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb6d-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb6d-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fb6d-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fb6d-111">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb6d-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb6d-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




