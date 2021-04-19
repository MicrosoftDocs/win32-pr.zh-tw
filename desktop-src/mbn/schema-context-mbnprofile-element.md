---
description: 指定設定資料連線所需的參數。
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: CoNtext (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984171"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="44799-103">CoNtext (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="44799-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="44799-104">**CoNtext (MBNProfile)** 元素會指定設定資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="44799-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="44799-105">專案可以有下列子項目。</span><span class="sxs-lookup"><span data-stu-id="44799-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="44799-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="44799-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="44799-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="44799-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="44799-108">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="44799-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="44799-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="44799-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="44799-110">此元素最多可有一次。</span><span class="sxs-lookup"><span data-stu-id="44799-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="44799-111">**CoNtext** 專案是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="44799-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="44799-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="44799-112">Requirements</span></span>



| <span data-ttu-id="44799-113">需求</span><span class="sxs-lookup"><span data-stu-id="44799-113">Requirement</span></span> | <span data-ttu-id="44799-114">值</span><span class="sxs-lookup"><span data-stu-id="44799-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="44799-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44799-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44799-116">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44799-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="44799-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44799-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44799-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="44799-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="44799-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44799-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="44799-120">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="44799-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="44799-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="44799-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="44799-122">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="44799-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="44799-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="44799-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




