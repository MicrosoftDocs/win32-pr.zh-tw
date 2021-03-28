---
description: 這個類別是系統呼叫 exit 事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973409"
---
# <a name="syscallexit-class"></a><span data-ttu-id="3a7f3-104">SysCallExit 類別</span><span class="sxs-lookup"><span data-stu-id="3a7f3-104">SysCallExit class</span></span>

<span data-ttu-id="3a7f3-105">這個類別是系統呼叫 exit 事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="3a7f3-105">This class is the event type class for system call exit events.</span></span>

<span data-ttu-id="3a7f3-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="3a7f3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a7f3-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a7f3-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a><span data-ttu-id="3a7f3-108">成員</span><span class="sxs-lookup"><span data-stu-id="3a7f3-108">Members</span></span>

<span data-ttu-id="3a7f3-109">**SysCallExit** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3a7f3-109">The **SysCallExit** class has these types of members:</span></span>

-   [<span data-ttu-id="3a7f3-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3a7f3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a7f3-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3a7f3-111">Properties</span></span>

<span data-ttu-id="3a7f3-112">**SysCallExit** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3a7f3-112">The **SysCallExit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a7f3-113">**SysCallNtStatus**</span><span class="sxs-lookup"><span data-stu-id="3a7f3-113">**SysCallNtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a7f3-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3a7f3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a7f3-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3a7f3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a7f3-116">限定詞： WmiDataId (1) ，格式 ( "x" ) </span><span class="sxs-lookup"><span data-stu-id="3a7f3-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="3a7f3-117">NT 系統呼叫所傳回的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="3a7f3-117">Status code returned by the NT system call.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a7f3-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a7f3-118">Requirements</span></span>



| <span data-ttu-id="3a7f3-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a7f3-119">Requirement</span></span> | <span data-ttu-id="3a7f3-120">值</span><span class="sxs-lookup"><span data-stu-id="3a7f3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a7f3-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a7f3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a7f3-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a7f3-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a7f3-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a7f3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a7f3-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a7f3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




