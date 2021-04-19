---
title: pathType 簡單類型
description: 定義定義檔案路徑之字串的最小和最大字元數。
ms.assetid: 09908f75-ba7b-4e31-877e-80fabea6bd27
keywords:
- pathType 簡單類型工作排程器
topic_type:
- apiref
api_name:
- pathType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a75ef7d85eba2aa39e0c3c768fec0908c7ea16b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970461"
---
# <a name="pathtype-simple-type"></a><span data-ttu-id="e4f93-104">pathType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="e4f93-104">pathType Simple Type</span></span>

<span data-ttu-id="e4f93-105">定義定義檔案路徑之字串的最小和最大字元數。</span><span class="sxs-lookup"><span data-stu-id="e4f93-105">Defines the minimum and maximum number of characters for a string that defines a file path.</span></span> <span data-ttu-id="e4f93-106">路徑不可以是空字串，而且必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="e4f93-106">The path cannot be an empty string, and must be less than 260 characters.</span></span>

``` syntax
<xs:simpleType name="pathType">
    <xs:restriction
        base="nonEmptyString"
    >
        <xs:maxLength
            value="260"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="e4f93-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4f93-107">Requirements</span></span>



| <span data-ttu-id="e4f93-108">需求</span><span class="sxs-lookup"><span data-stu-id="e4f93-108">Requirement</span></span> | <span data-ttu-id="e4f93-109">值</span><span class="sxs-lookup"><span data-stu-id="e4f93-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e4f93-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4f93-110">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f93-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4f93-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e4f93-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4f93-112">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f93-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4f93-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





