---
description: 指定用來驗證使用者的密碼。
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: 密碼 (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997084"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="8dca4-103">密碼 (UserLogonCred) 元素</span><span class="sxs-lookup"><span data-stu-id="8dca4-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="8dca4-104">[**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md)元素會指定用來驗證使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="8dca4-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="8dca4-105">元素是最多255個字元的字串。</span><span class="sxs-lookup"><span data-stu-id="8dca4-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="8dca4-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="8dca4-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="8dca4-107">**Password** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="8dca4-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dca4-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dca4-108">Requirements</span></span>



| <span data-ttu-id="8dca4-109">需求</span><span class="sxs-lookup"><span data-stu-id="8dca4-109">Requirement</span></span> | <span data-ttu-id="8dca4-110">值</span><span class="sxs-lookup"><span data-stu-id="8dca4-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="8dca4-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8dca4-111">Minimum supported client</span></span><br/> | <span data-ttu-id="8dca4-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dca4-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="8dca4-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8dca4-113">Minimum supported server</span></span><br/> | <span data-ttu-id="8dca4-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="8dca4-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="8dca4-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dca4-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="8dca4-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="8dca4-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8dca4-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="8dca4-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="8dca4-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="8dca4-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8dca4-119">**UserLogonCred (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="8dca4-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




