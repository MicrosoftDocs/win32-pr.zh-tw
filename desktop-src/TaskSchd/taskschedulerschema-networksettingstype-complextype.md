---
title: networkSettingsType 複雜類型
description: 定義元素，這些專案提供工作排程器服務用來取得網路設定檔的設定。
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- networkSettingsType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934590"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="5a0cc-104">networkSettingsType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="5a0cc-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="5a0cc-105">定義元素，這些專案提供工作排程器服務用來取得網路設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="5a0cc-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5a0cc-106">子元素</span><span class="sxs-lookup"><span data-stu-id="5a0cc-106">Child elements</span></span>



| <span data-ttu-id="5a0cc-107">元素</span><span class="sxs-lookup"><span data-stu-id="5a0cc-107">Element</span></span>                                                              | <span data-ttu-id="5a0cc-108">類型</span><span class="sxs-lookup"><span data-stu-id="5a0cc-108">Type</span></span>                                                        | <span data-ttu-id="5a0cc-109">Description</span><span class="sxs-lookup"><span data-stu-id="5a0cc-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a0cc-110">**Id**</span><span class="sxs-lookup"><span data-stu-id="5a0cc-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="5a0cc-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="5a0cc-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="5a0cc-112">指定可識別網路設定檔的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="5a0cc-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="5a0cc-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="5a0cc-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="5a0cc-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="5a0cc-114">nonEmptyString</span></span>                                              | <span data-ttu-id="5a0cc-115">指定網路設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a0cc-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="5a0cc-116">此名稱會用於顯示用途。</span><span class="sxs-lookup"><span data-stu-id="5a0cc-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="5a0cc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a0cc-117">Requirements</span></span>



| <span data-ttu-id="5a0cc-118">需求</span><span class="sxs-lookup"><span data-stu-id="5a0cc-118">Requirement</span></span> | <span data-ttu-id="5a0cc-119">值</span><span class="sxs-lookup"><span data-stu-id="5a0cc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5a0cc-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a0cc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a0cc-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a0cc-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5a0cc-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a0cc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a0cc-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a0cc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





