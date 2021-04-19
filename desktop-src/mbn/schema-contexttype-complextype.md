---
description: 指定行動寬頻裝置的 connenction 內容。
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: coNtextType 複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973452"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="1515b-103">coNtextType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="1515b-103">contextType Complex Type</span></span>

<span data-ttu-id="1515b-104">**CoNtextType** 複雜類型會指定行動寬頻裝置的 connenction 內容。</span><span class="sxs-lookup"><span data-stu-id="1515b-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
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
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1515b-105">子元素</span><span class="sxs-lookup"><span data-stu-id="1515b-105">Child elements</span></span>



| <span data-ttu-id="1515b-106">元素</span><span class="sxs-lookup"><span data-stu-id="1515b-106">Element</span></span>                                                               | <span data-ttu-id="1515b-107">類型</span><span class="sxs-lookup"><span data-stu-id="1515b-107">Type</span></span>                                           | <span data-ttu-id="1515b-108">Description</span><span class="sxs-lookup"><span data-stu-id="1515b-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1515b-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="1515b-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="1515b-110">用來建立資料連線的 APN 或撥號字串</span><span class="sxs-lookup"><span data-stu-id="1515b-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="1515b-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="1515b-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="1515b-112">用來啟用 PDP 內容的驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1515b-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="1515b-113">**壓縮**</span><span class="sxs-lookup"><span data-stu-id="1515b-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="1515b-114">指定壓縮是否會用於標頭和資料傳輸的資料連結</span><span class="sxs-lookup"><span data-stu-id="1515b-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="1515b-115">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="1515b-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="1515b-116">boolean</span><span class="sxs-lookup"><span data-stu-id="1515b-116">boolean</span></span>                                        | <span data-ttu-id="1515b-117">如何在升級設定檔時處理密碼。</span><span class="sxs-lookup"><span data-stu-id="1515b-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="1515b-118">**密碼**</span><span class="sxs-lookup"><span data-stu-id="1515b-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="1515b-119">字串</span><span class="sxs-lookup"><span data-stu-id="1515b-119">string</span></span>                                         | <span data-ttu-id="1515b-120">用來驗證使用者的密碼</span><span class="sxs-lookup"><span data-stu-id="1515b-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="1515b-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="1515b-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="1515b-122">登入連接的認證。</span><span class="sxs-lookup"><span data-stu-id="1515b-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="1515b-123">**使用者**</span><span class="sxs-lookup"><span data-stu-id="1515b-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="1515b-124">**nameType**</span><span class="sxs-lookup"><span data-stu-id="1515b-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="1515b-125">登入的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="1515b-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="1515b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1515b-126">Requirements</span></span>



| <span data-ttu-id="1515b-127">需求</span><span class="sxs-lookup"><span data-stu-id="1515b-127">Requirement</span></span> | <span data-ttu-id="1515b-128">值</span><span class="sxs-lookup"><span data-stu-id="1515b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="1515b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1515b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1515b-130">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1515b-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="1515b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1515b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1515b-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="1515b-132">None supported</span></span><br/>                         |



 

 




