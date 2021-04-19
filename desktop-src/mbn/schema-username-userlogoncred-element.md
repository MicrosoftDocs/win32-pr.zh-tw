---
description: 指定登入的使用者名稱。
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: UserName (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991820"
---
# <a name="username-userlogoncred-element"></a><span data-ttu-id="3d25e-103">UserName (UserLogonCred) 元素</span><span class="sxs-lookup"><span data-stu-id="3d25e-103">UserName (UserLogonCred) Element</span></span>

<span data-ttu-id="3d25e-104">**UserName (UserLogonCred)** 元素會指定登入的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="3d25e-104">The **UserName (UserLogonCred)** element specifies the user name for logon.</span></span>

<span data-ttu-id="3d25e-105">元素是最多255個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="3d25e-105">The element is a string with a maximum of 255 characters.</span></span>

<span data-ttu-id="3d25e-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="3d25e-106">This element is optional.</span></span>

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

<span data-ttu-id="3d25e-107">**UserName** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="3d25e-107">The **UserName** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d25e-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d25e-108">Requirements</span></span>



| <span data-ttu-id="3d25e-109">需求</span><span class="sxs-lookup"><span data-stu-id="3d25e-109">Requirement</span></span> | <span data-ttu-id="3d25e-110">值</span><span class="sxs-lookup"><span data-stu-id="3d25e-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="3d25e-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d25e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="3d25e-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d25e-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3d25e-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d25e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="3d25e-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="3d25e-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3d25e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d25e-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d25e-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="3d25e-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3d25e-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="3d25e-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="3d25e-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="3d25e-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3d25e-119">**UserLogonCred (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="3d25e-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




