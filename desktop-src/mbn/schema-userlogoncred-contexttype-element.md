---
description: 包含連接的登入認證。
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: UserLogonCred (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113448"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="9b4df-103">UserLogonCred (coNtextType) 元素</span><span class="sxs-lookup"><span data-stu-id="9b4df-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="9b4df-104">**UserLogonCred (coNtextType)** 元素包含連接的登入認證。</span><span class="sxs-lookup"><span data-stu-id="9b4df-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="9b4df-105">這個元素可以有下列子項目。</span><span class="sxs-lookup"><span data-stu-id="9b4df-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="9b4df-106">**使用者**</span><span class="sxs-lookup"><span data-stu-id="9b4df-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="9b4df-107">**密碼**</span><span class="sxs-lookup"><span data-stu-id="9b4df-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="9b4df-108">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="9b4df-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="9b4df-109">此元素最多可有一次。</span><span class="sxs-lookup"><span data-stu-id="9b4df-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="9b4df-110">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="9b4df-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="9b4df-111">**UserLogonCred** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="9b4df-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="9b4df-112">子元素</span><span class="sxs-lookup"><span data-stu-id="9b4df-112">Child elements</span></span>



| <span data-ttu-id="9b4df-113">元素</span><span class="sxs-lookup"><span data-stu-id="9b4df-113">Element</span></span>                                                               | <span data-ttu-id="9b4df-114">類型</span><span class="sxs-lookup"><span data-stu-id="9b4df-114">Type</span></span>                                           | <span data-ttu-id="9b4df-115">Description</span><span class="sxs-lookup"><span data-stu-id="9b4df-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="9b4df-116">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="9b4df-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="9b4df-117">boolean</span><span class="sxs-lookup"><span data-stu-id="9b4df-117">boolean</span></span>                                        | <span data-ttu-id="9b4df-118">如何在升級設定檔時處理密碼。</span><span class="sxs-lookup"><span data-stu-id="9b4df-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="9b4df-119">**密碼**</span><span class="sxs-lookup"><span data-stu-id="9b4df-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="9b4df-120">字串</span><span class="sxs-lookup"><span data-stu-id="9b4df-120">string</span></span>                                         | <span data-ttu-id="9b4df-121">使用者密碼。</span><span class="sxs-lookup"><span data-stu-id="9b4df-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="9b4df-122">**使用者**</span><span class="sxs-lookup"><span data-stu-id="9b4df-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="9b4df-123">**nameType**</span><span class="sxs-lookup"><span data-stu-id="9b4df-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="9b4df-124">使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="9b4df-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="9b4df-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b4df-125">Requirements</span></span>



| <span data-ttu-id="9b4df-126">需求</span><span class="sxs-lookup"><span data-stu-id="9b4df-126">Requirement</span></span> | <span data-ttu-id="9b4df-127">值</span><span class="sxs-lookup"><span data-stu-id="9b4df-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="9b4df-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b4df-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b4df-129">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b4df-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="9b4df-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b4df-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b4df-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="9b4df-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="9b4df-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b4df-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b4df-133">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="9b4df-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9b4df-134">**coNtextType**</span><span class="sxs-lookup"><span data-stu-id="9b4df-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="9b4df-135">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="9b4df-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9b4df-136">**MBNProfile) 內容 (**</span><span class="sxs-lookup"><span data-stu-id="9b4df-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




