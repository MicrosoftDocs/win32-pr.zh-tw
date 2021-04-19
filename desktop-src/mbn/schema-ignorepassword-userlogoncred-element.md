---
description: 指定如何在升級設定檔時處理密碼。
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: IgnorePassword (UserLogonCred) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966729"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="cc240-103">IgnorePassword (UserLogonCred) 元素</span><span class="sxs-lookup"><span data-stu-id="cc240-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="cc240-104">**IgnorePassword (UserLogonCred)** 元素會指定如何在升級設定檔時處理密碼。</span><span class="sxs-lookup"><span data-stu-id="cc240-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="cc240-105">如果設定為 **TRUE** 且在更新作業時存在具有相同名稱的設定檔，則會採用該設定檔中的密碼，並將其儲存在新的設定檔中。</span><span class="sxs-lookup"><span data-stu-id="cc240-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="cc240-106">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="cc240-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="cc240-107">**IgnorePassword** 元素是由 [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="cc240-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc240-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc240-108">Requirements</span></span>



| <span data-ttu-id="cc240-109">需求</span><span class="sxs-lookup"><span data-stu-id="cc240-109">Requirement</span></span> | <span data-ttu-id="cc240-110">值</span><span class="sxs-lookup"><span data-stu-id="cc240-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="cc240-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc240-111">Minimum supported client</span></span><br/> | <span data-ttu-id="cc240-112">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc240-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="cc240-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc240-113">Minimum supported server</span></span><br/> | <span data-ttu-id="cc240-114">都不支援</span><span class="sxs-lookup"><span data-stu-id="cc240-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="cc240-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc240-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc240-116">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="cc240-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cc240-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="cc240-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="cc240-118">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="cc240-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cc240-119">**UserLogonCred (coNtextType)**</span><span class="sxs-lookup"><span data-stu-id="cc240-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




