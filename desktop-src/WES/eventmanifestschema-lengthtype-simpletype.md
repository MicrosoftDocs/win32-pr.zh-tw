---
title: LengthType 簡單類型
description: 定義長度類型，這個類型會用來指定變數長度資料項目（例如二進位資料或 ANSI 或 Unicode 字串）中的位元組或字元數目。
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- LengthType 簡單類型 EventLog
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317459"
---
# <a name="lengthtype-simple-type"></a><span data-ttu-id="5ef20-104">LengthType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="5ef20-104">LengthType Simple Type</span></span>

<span data-ttu-id="5ef20-105">定義長度類型，這個類型會用來指定變數長度資料項目（例如二進位資料或 ANSI 或 Unicode 字串）中的位元組或字元數目。</span><span class="sxs-lookup"><span data-stu-id="5ef20-105">Defines a length type that is used to specify the number of bytes or characters in a variable length data item such as binary data or an ANSI or Unicode string.</span></span> <span data-ttu-id="5ef20-106">值可以指定為 xs： unsignedShort 值，或指定為參考包含不帶正負號短值之資料項目節點名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5ef20-106">The value can be specified as an xs:unsignedShort value or as a string that references the name of data item node that contains the unsigned short value.</span></span>

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="5ef20-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ef20-107">Requirements</span></span>



| <span data-ttu-id="5ef20-108">需求</span><span class="sxs-lookup"><span data-stu-id="5ef20-108">Requirement</span></span> | <span data-ttu-id="5ef20-109">值</span><span class="sxs-lookup"><span data-stu-id="5ef20-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ef20-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ef20-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef20-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ef20-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ef20-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ef20-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef20-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ef20-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





