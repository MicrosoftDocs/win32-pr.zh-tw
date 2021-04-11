---
description: 指定是否快取使用者認證以進行後續連接。
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: cacheUserData (OneX) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944148"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="c9e3e-103">cacheUserData (OneX) 元素</span><span class="sxs-lookup"><span data-stu-id="c9e3e-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="c9e3e-104">CacheUserData (OneX) 元素會指定是否要快取使用者認證以進行後續連接。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="c9e3e-105">當 cacheUserData 為 TRUE 時，會快取認證。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="c9e3e-106">當 cacheUserData 為 FALSE 時，將不會快取認證，而且使用者可能會在後續連接嘗試時提示您輸入認證。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="c9e3e-107">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-107">This element is optional.</span></span> <span data-ttu-id="c9e3e-108">當設定檔中未指定 cacheUserData 時，會快取使用者認證。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="c9e3e-109">Windows **xp （含 SP3）和適用于 WINDOWS XP SP2 的無線區域網路 API：** 如果設定檔中有此元素，將會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="c9e3e-110">**CacheUserData** 元素是由 [**OneX**](onexschema-onex-element.md)元素所定義。</span><span class="sxs-lookup"><span data-stu-id="c9e3e-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9e3e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9e3e-111">Requirements</span></span>



| <span data-ttu-id="c9e3e-112">需求</span><span class="sxs-lookup"><span data-stu-id="c9e3e-112">Requirement</span></span> | <span data-ttu-id="c9e3e-113">值</span><span class="sxs-lookup"><span data-stu-id="c9e3e-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9e3e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9e3e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e3e-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9e3e-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9e3e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9e3e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e3e-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9e3e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9e3e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9e3e-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9e3e-119">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="c9e3e-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c9e3e-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="c9e3e-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="c9e3e-121">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="c9e3e-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c9e3e-122">**OneX**</span><span class="sxs-lookup"><span data-stu-id="c9e3e-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




