---
title: attachmentsType 複雜類型
description: 定義用來指定與電子郵件訊息一起傳送之附件的元素。
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- attachmentsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999610"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="15200-104">attachmentsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="15200-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="15200-105">定義用來指定與電子郵件訊息一起傳送之附件的元素。</span><span class="sxs-lookup"><span data-stu-id="15200-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="15200-106">子元素</span><span class="sxs-lookup"><span data-stu-id="15200-106">Child elements</span></span>



| <span data-ttu-id="15200-107">元素</span><span class="sxs-lookup"><span data-stu-id="15200-107">Element</span></span>                                                          | <span data-ttu-id="15200-108">類型</span><span class="sxs-lookup"><span data-stu-id="15200-108">Type</span></span>                                                                    | <span data-ttu-id="15200-109">Description</span><span class="sxs-lookup"><span data-stu-id="15200-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15200-110">**檔案**</span><span class="sxs-lookup"><span data-stu-id="15200-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="15200-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="15200-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="15200-112">指定以電子郵件訊息中的附件形式傳送之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="15200-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="15200-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="15200-113">Requirements</span></span>



| <span data-ttu-id="15200-114">需求</span><span class="sxs-lookup"><span data-stu-id="15200-114">Requirement</span></span> | <span data-ttu-id="15200-115">值</span><span class="sxs-lookup"><span data-stu-id="15200-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15200-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15200-116">Minimum supported client</span></span><br/> | <span data-ttu-id="15200-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15200-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="15200-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15200-118">Minimum supported server</span></span><br/> | <span data-ttu-id="15200-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15200-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





