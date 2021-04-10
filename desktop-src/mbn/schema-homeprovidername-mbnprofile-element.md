---
description: 識別指定之 SIM/裝置的家用提供者名稱。
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: HomeProviderName (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690323"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="35858-103">HomeProviderName (MBNProfile) 元素</span><span class="sxs-lookup"><span data-stu-id="35858-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="35858-104">**HomeProviderName (MBNProfile)** 元素會識別給定 SIM/裝置的家用提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="35858-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="35858-105">這個元素是選擇性的，且由行動寬頻服務設定供內部使用。</span><span class="sxs-lookup"><span data-stu-id="35858-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="35858-106">應用程式在建立或更新設定檔時，不應設定此欄位。</span><span class="sxs-lookup"><span data-stu-id="35858-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="35858-107">**HomeProviderName** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="35858-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="35858-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="35858-108">Requirements</span></span>



| <span data-ttu-id="35858-109">需求</span><span class="sxs-lookup"><span data-stu-id="35858-109">Requirement</span></span> | <span data-ttu-id="35858-110">值</span><span class="sxs-lookup"><span data-stu-id="35858-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="35858-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35858-111">Minimum supported client</span></span><br/> | <span data-ttu-id="35858-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35858-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="35858-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35858-113">Minimum supported server</span></span><br/> | <span data-ttu-id="35858-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="35858-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="35858-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35858-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="35858-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="35858-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="35858-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="35858-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="35858-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="35858-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="35858-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="35858-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




