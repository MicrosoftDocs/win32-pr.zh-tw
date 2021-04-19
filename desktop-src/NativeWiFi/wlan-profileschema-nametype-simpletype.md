---
description: 包含無線局域網路設定檔的名稱或描述。
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: 'nameType 簡單類型 (LAN_policy)  (設定檔) '
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
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "107001052"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="ff5a5-103">針對 profileschema nameType 簡單類型 (LAN_policy) </span><span class="sxs-lookup"><span data-stu-id="ff5a5-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="ff5a5-104">NameType 簡單類型可以包含無線局域網路設定檔的名稱或描述。</span><span class="sxs-lookup"><span data-stu-id="ff5a5-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="ff5a5-105">這個字串值的長度必須介於1到255個字元之間。</span><span class="sxs-lookup"><span data-stu-id="ff5a5-105">This string value must be between 1 and 255 characters long.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="ff5a5-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff5a5-106">Requirements</span></span>



| <span data-ttu-id="ff5a5-107">需求</span><span class="sxs-lookup"><span data-stu-id="ff5a5-107">Requirement</span></span> | <span data-ttu-id="ff5a5-108">值</span><span class="sxs-lookup"><span data-stu-id="ff5a5-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ff5a5-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff5a5-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ff5a5-110">Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff5a5-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ff5a5-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff5a5-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ff5a5-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff5a5-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ff5a5-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ff5a5-113">Redistributable</span></span><br/>          | <span data-ttu-id="ff5a5-114">適用于 Windows XP SP2 的無線區域網路 API</span><span class="sxs-lookup"><span data-stu-id="ff5a5-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




