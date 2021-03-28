---
description: HWConfig \_ NIC 類別是網路介面卡設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027334"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="6b6c9-104">HWConfig \_ NIC 類別</span><span class="sxs-lookup"><span data-stu-id="6b6c9-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="6b6c9-105">**HWConfig \_ NIC** 類別是網路介面卡設定事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="6b6c9-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="6b6c9-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6b6c9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6c9-107">語法</span><span class="sxs-lookup"><span data-stu-id="6b6c9-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="6b6c9-108">成員</span><span class="sxs-lookup"><span data-stu-id="6b6c9-108">Members</span></span>

<span data-ttu-id="6b6c9-109">**HWConfig \_ NIC** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6b6c9-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="6b6c9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6b6c9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b6c9-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6b6c9-111">Properties</span></span>

<span data-ttu-id="6b6c9-112">**HWConfig \_ NIC** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6b6c9-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b6c9-113">NICName</span><span class="sxs-lookup"><span data-stu-id="6b6c9-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c9-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6b6c9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c9-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6b6c9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b6c9-116">限定詞： WmiDataId (1) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) </span><span class="sxs-lookup"><span data-stu-id="6b6c9-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="6b6c9-117">網路介面卡的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b6c9-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b6c9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b6c9-118">Requirements</span></span>



| <span data-ttu-id="6b6c9-119">需求</span><span class="sxs-lookup"><span data-stu-id="6b6c9-119">Requirement</span></span> | <span data-ttu-id="6b6c9-120">值</span><span class="sxs-lookup"><span data-stu-id="6b6c9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="6b6c9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b6c9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6c9-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b6c9-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6b6c9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b6c9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6c9-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="6b6c9-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="6b6c9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b6c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6c9-126">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="6b6c9-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




