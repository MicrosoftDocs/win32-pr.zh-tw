---
title: QNameList 簡單類型
description: 定義限定名稱的清單。
ms.assetid: 727d87a0-82f5-44fa-a841-4c2445f78063
keywords:
- QNameList 簡單類型 EventLog
topic_type:
- apiref
api_name:
- QNameList
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcb078c2fcddd9b1549ff095820ce19eb7d5a13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685464"
---
# <a name="qnamelist-simple-type"></a><span data-ttu-id="1e1bc-104">QNameList 簡單類型</span><span class="sxs-lookup"><span data-stu-id="1e1bc-104">QNameList Simple Type</span></span>

<span data-ttu-id="1e1bc-105">定義限定名稱的清單。</span><span class="sxs-lookup"><span data-stu-id="1e1bc-105">Defines a list of qualified names.</span></span>

``` syntax
<xs:simpleType name="QNameList">
    <xs:list>
        <xs:itemType name="QName" />
    </xs:list>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="1e1bc-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e1bc-106">Requirements</span></span>



| <span data-ttu-id="1e1bc-107">需求</span><span class="sxs-lookup"><span data-stu-id="1e1bc-107">Requirement</span></span> | <span data-ttu-id="1e1bc-108">值</span><span class="sxs-lookup"><span data-stu-id="1e1bc-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e1bc-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e1bc-109">Minimum supported client</span></span><br/> | <span data-ttu-id="1e1bc-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e1bc-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e1bc-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e1bc-111">Minimum supported server</span></span><br/> | <span data-ttu-id="1e1bc-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e1bc-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





