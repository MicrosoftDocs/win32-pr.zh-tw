---
description: 定義行動寬頻設定檔中 ICONFilePath 元素的字串類型。
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: iconFileType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112897"
---
# <a name="iconfiletype-simple-type"></a><span data-ttu-id="d7cd3-103">iconFileType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="d7cd3-103">iconFileType Simple Type</span></span>

<span data-ttu-id="d7cd3-104">**IconFileType** 簡單類型會定義行動寬頻設定檔中 [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)元素的字串類型。</span><span class="sxs-lookup"><span data-stu-id="d7cd3-104">The **iconFileType** simple type defines a string type for the [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) element in the Mobile Broadband profile.</span></span> <span data-ttu-id="d7cd3-105">這個字串的長度至少要有一個字元，且長度最多為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="d7cd3-105">This string is at least one character long and at most 1024 characters long.</span></span>

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="d7cd3-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7cd3-106">Requirements</span></span>



| <span data-ttu-id="d7cd3-107">需求</span><span class="sxs-lookup"><span data-stu-id="d7cd3-107">Requirement</span></span> | <span data-ttu-id="d7cd3-108">值</span><span class="sxs-lookup"><span data-stu-id="d7cd3-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d7cd3-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7cd3-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d7cd3-110">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7cd3-110">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d7cd3-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7cd3-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d7cd3-112">都不支援</span><span class="sxs-lookup"><span data-stu-id="d7cd3-112">None supported</span></span><br/>                         |



 

 




