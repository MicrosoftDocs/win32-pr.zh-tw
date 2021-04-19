---
description: 定義計數器的屬性，指定如何在取用者應用程式中顯示計數器資料。
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: counterAttribute 複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979152"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="b603f-103">counterAttribute 複雜類型</span><span class="sxs-lookup"><span data-stu-id="b603f-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="b603f-104">定義計數器的屬性，指定如何在取用者應用程式中顯示計數器資料。</span><span class="sxs-lookup"><span data-stu-id="b603f-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="b603f-105">屬性</span><span class="sxs-lookup"><span data-stu-id="b603f-105">Attributes</span></span>



| <span data-ttu-id="b603f-106">名稱</span><span class="sxs-lookup"><span data-stu-id="b603f-106">Name</span></span> | <span data-ttu-id="b603f-107">類型</span><span class="sxs-lookup"><span data-stu-id="b603f-107">Type</span></span> | <span data-ttu-id="b603f-108">描述</span><span class="sxs-lookup"><span data-stu-id="b603f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b603f-109">NAME</span><span class="sxs-lookup"><span data-stu-id="b603f-109">name</span></span> |      | <span data-ttu-id="b603f-110">要套用之顯示內容的名稱。</span><span class="sxs-lookup"><span data-stu-id="b603f-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="b603f-111">您可以指定下列其中一個名稱：</span><span class="sxs-lookup"><span data-stu-id="b603f-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="b603f-112"><dt><span id="reference"></span><span id="REFERENCE"></span>參考</dt></span><span class="sxs-lookup"><span data-stu-id="b603f-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="b603f-113">以傳址方式抓取計數器的值，而不是依值。</span><span class="sxs-lookup"><span data-stu-id="b603f-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="b603f-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span><span class="sxs-lookup"><span data-stu-id="b603f-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="b603f-115">不要顯示計數器值。</span><span class="sxs-lookup"><span data-stu-id="b603f-115">Do not display the counter value.</span></span> <span data-ttu-id="b603f-116">一般而言，如果計數器的資料是用來做為計算其他計數器值的輸入，您就會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="b603f-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="b603f-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span><span class="sxs-lookup"><span data-stu-id="b603f-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="b603f-118">顯示計數器值時，取用者或監視應用程式不應使用數位分隔符號。</span><span class="sxs-lookup"><span data-stu-id="b603f-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="b603f-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span><span class="sxs-lookup"><span data-stu-id="b603f-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="b603f-120">取用者或監視應用程式應該以十六進位（而非預設整數值）顯示計數器值。</span><span class="sxs-lookup"><span data-stu-id="b603f-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="b603f-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span><span class="sxs-lookup"><span data-stu-id="b603f-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="b603f-122">取用者或監視應用程式應該將計數器值顯示為實數，而非預設整數值。</span><span class="sxs-lookup"><span data-stu-id="b603f-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="b603f-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b603f-123">Requirements</span></span>



| <span data-ttu-id="b603f-124">需求</span><span class="sxs-lookup"><span data-stu-id="b603f-124">Requirement</span></span> | <span data-ttu-id="b603f-125">值</span><span class="sxs-lookup"><span data-stu-id="b603f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b603f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b603f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b603f-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b603f-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b603f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b603f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b603f-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b603f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




