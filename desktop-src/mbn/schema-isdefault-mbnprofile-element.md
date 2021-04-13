---
description: 指定這是否為裝置的預設設定檔。
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: IsDefault (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469000"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="2d3a8-103">IsDefault (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="2d3a8-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="2d3a8-104">**IsDefault (MBNProfile)** 元素會指定這是否為裝置的預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="2d3a8-105">這是選擇性專案，如果未指定，則不會將設定檔設定為預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="2d3a8-106">行動寬頻服務會使用預設設定檔進行下列用途</span><span class="sxs-lookup"><span data-stu-id="2d3a8-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="2d3a8-107">行動寬頻服務在執行自動網路連線時，會使用預設設定檔中的連線設定。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="2d3a8-108">這些設定包括存取點名稱、使用者名稱、密碼等等。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="2d3a8-109">行動寬頻裝置的自動連線原則是取自其預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="2d3a8-110">作業系統網路連線 UI 也會使用連接作業的預設設定檔中的連接資料。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="2d3a8-111">行動電話服務提供者可以在設定檔中提供連線詳細資料，並將該設定檔設定為預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="2d3a8-112">行動寬頻服務將會使用這些連接設定，而不會提示使用者提供詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="2d3a8-113">**IsDefault** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="2d3a8-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3a8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d3a8-114">Requirements</span></span>



| <span data-ttu-id="2d3a8-115">需求</span><span class="sxs-lookup"><span data-stu-id="2d3a8-115">Requirement</span></span> | <span data-ttu-id="2d3a8-116">值</span><span class="sxs-lookup"><span data-stu-id="2d3a8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2d3a8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d3a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3a8-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d3a8-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2d3a8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d3a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3a8-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="2d3a8-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="2d3a8-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d3a8-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d3a8-122">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2d3a8-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="2d3a8-124">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2d3a8-125">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2d3a8-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




