---
description: 定義行動寬頻設定檔之 SimIccID 元素的類型。
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: simIccIDType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000248"
---
# <a name="simiccidtype-simple-type"></a><span data-ttu-id="30724-103">simIccIDType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="30724-103">simIccIDType Simple Type</span></span>

<span data-ttu-id="30724-104">**SimIccIDType** 簡單類型會定義行動寬頻設定檔的 [**SimIccID**](schema-simiccid-mbnprofile-element.md)元素類型。</span><span class="sxs-lookup"><span data-stu-id="30724-104">The **simIccIDType** simple type defines a type for the [**SimIccID**](schema-simiccid-mbnprofile-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="30724-105">此類型是數位和/或大寫和小寫字母的集合，至少一個字元長，最多20個字元。</span><span class="sxs-lookup"><span data-stu-id="30724-105">This type is a collection of digits and/or upper- and lower-case letters, at least one character long and at most 20 characters long.</span></span>

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="30724-106">模式</span><span class="sxs-lookup"><span data-stu-id="30724-106">Patterns</span></span>

<span data-ttu-id="30724-107">**SimIccIDType** 簡單類型是以下列模式限制的標記：</span><span class="sxs-lookup"><span data-stu-id="30724-107">The **simIccIDType** simple type is a token that is restricted by the following pattern:</span></span>

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a><span data-ttu-id="30724-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="30724-108">Requirements</span></span>



| <span data-ttu-id="30724-109">需求</span><span class="sxs-lookup"><span data-stu-id="30724-109">Requirement</span></span> | <span data-ttu-id="30724-110">值</span><span class="sxs-lookup"><span data-stu-id="30724-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="30724-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30724-111">Minimum supported client</span></span><br/> | <span data-ttu-id="30724-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30724-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="30724-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30724-113">Minimum supported server</span></span><br/> | <span data-ttu-id="30724-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="30724-114">None supported</span></span><br/>                         |



 

 




