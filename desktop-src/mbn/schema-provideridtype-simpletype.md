---
description: 定義 Mobile 寬頻設定檔的 ProviderID 元素類型。
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: providerIdType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112892"
---
# <a name="provideridtype-simple-type"></a><span data-ttu-id="a7667-103">providerIdType 簡單類型</span><span class="sxs-lookup"><span data-stu-id="a7667-103">providerIdType Simple Type</span></span>

<span data-ttu-id="a7667-104">**ProviderIdType** simple type 會定義 Mobile 寬頻設定檔的 [**ProviderID**](schema-providerid-providertype-element.md)元素類型。</span><span class="sxs-lookup"><span data-stu-id="a7667-104">The **providerIdType** simple type defines a type for the [**ProviderID**](schema-providerid-providertype-element.md) element of the Mobile Broadband profile.</span></span> <span data-ttu-id="a7667-105">此類型是至少一個數位的集合，且長度最多為6位數。</span><span class="sxs-lookup"><span data-stu-id="a7667-105">This type is a collection of digits at least one digit long and at most 6 digits long.</span></span>

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="a7667-106">模式</span><span class="sxs-lookup"><span data-stu-id="a7667-106">Patterns</span></span>

<span data-ttu-id="a7667-107">**ProviderIdType** 簡單類型是以下列模式限制的標記：</span><span class="sxs-lookup"><span data-stu-id="a7667-107">The **providerIdType** simple type is a token that is restricted by the following pattern:</span></span>

-   `\d{1,6}`

## <a name="requirements"></a><span data-ttu-id="a7667-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7667-108">Requirements</span></span>



| <span data-ttu-id="a7667-109">需求</span><span class="sxs-lookup"><span data-stu-id="a7667-109">Requirement</span></span> | <span data-ttu-id="a7667-110">值</span><span class="sxs-lookup"><span data-stu-id="a7667-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a7667-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7667-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a7667-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7667-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a7667-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7667-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a7667-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="a7667-114">None supported</span></span><br/>                         |



 

 




