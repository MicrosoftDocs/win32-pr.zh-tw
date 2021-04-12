---
title: filePath 簡單類型
description: 定義包含檔案完整路徑的字串。
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- filePath simple type EventLog
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464569"
---
# <a name="filepath-simple-type"></a><span data-ttu-id="9516b-104">filePath 簡單類型</span><span class="sxs-lookup"><span data-stu-id="9516b-104">filePath Simple Type</span></span>

<span data-ttu-id="9516b-105">定義包含檔案完整路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="9516b-105">Defines a string that contains a fully qualified path to a file.</span></span> <span data-ttu-id="9516b-106">路徑可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="9516b-106">The path may contain environment variables.</span></span>

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="9516b-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="9516b-107">Requirements</span></span>



| <span data-ttu-id="9516b-108">需求</span><span class="sxs-lookup"><span data-stu-id="9516b-108">Requirement</span></span> | <span data-ttu-id="9516b-109">值</span><span class="sxs-lookup"><span data-stu-id="9516b-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9516b-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9516b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9516b-111">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9516b-111">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9516b-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9516b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9516b-113">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9516b-113">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





