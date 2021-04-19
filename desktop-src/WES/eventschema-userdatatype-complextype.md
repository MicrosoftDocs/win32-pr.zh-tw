---
title: UserDataType 複雜類型
description: 定義指定事件資料版面配置的 XML 片段。
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- UserDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967950"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="40b99-104">UserDataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="40b99-104">UserDataType Complex Type</span></span>

<span data-ttu-id="40b99-105">定義指定事件資料版面配置的 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="40b99-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="40b99-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="40b99-106">Requirements</span></span>



| <span data-ttu-id="40b99-107">需求</span><span class="sxs-lookup"><span data-stu-id="40b99-107">Requirement</span></span> | <span data-ttu-id="40b99-108">值</span><span class="sxs-lookup"><span data-stu-id="40b99-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40b99-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40b99-109">Minimum supported client</span></span><br/> | <span data-ttu-id="40b99-110">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40b99-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40b99-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40b99-111">Minimum supported server</span></span><br/> | <span data-ttu-id="40b99-112">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40b99-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





