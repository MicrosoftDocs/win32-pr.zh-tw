---
description: 此類別是系統呼叫輸入事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: SysCallEnter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1497491de622e564b945e8a80fcb1d8755886f39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973412"
---
# <a name="syscallenter-class"></a><span data-ttu-id="21982-104">SysCallEnter 類別</span><span class="sxs-lookup"><span data-stu-id="21982-104">SysCallEnter class</span></span>

<span data-ttu-id="21982-105">此類別是系統呼叫輸入事件的事件種類類別。</span><span class="sxs-lookup"><span data-stu-id="21982-105">This class is the event type class for system call enter events.</span></span>

<span data-ttu-id="21982-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="21982-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="21982-107">語法</span><span class="sxs-lookup"><span data-stu-id="21982-107">Syntax</span></span>

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a><span data-ttu-id="21982-108">成員</span><span class="sxs-lookup"><span data-stu-id="21982-108">Members</span></span>

<span data-ttu-id="21982-109">**SysCallEnter** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="21982-109">The **SysCallEnter** class has these types of members:</span></span>

-   [<span data-ttu-id="21982-110">屬性</span><span class="sxs-lookup"><span data-stu-id="21982-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21982-111">屬性</span><span class="sxs-lookup"><span data-stu-id="21982-111">Properties</span></span>

<span data-ttu-id="21982-112">**SysCallEnter** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="21982-112">The **SysCallEnter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21982-113">**SysCallAddress**</span><span class="sxs-lookup"><span data-stu-id="21982-113">**SysCallAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21982-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="21982-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21982-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="21982-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21982-116">限定詞： WmiDataId (1) ，指標</span><span class="sxs-lookup"><span data-stu-id="21982-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="21982-117">所輸入 NT 函式呼叫的位址。</span><span class="sxs-lookup"><span data-stu-id="21982-117">Address of the NT function call that is being entered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21982-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="21982-118">Requirements</span></span>



| <span data-ttu-id="21982-119">需求</span><span class="sxs-lookup"><span data-stu-id="21982-119">Requirement</span></span> | <span data-ttu-id="21982-120">值</span><span class="sxs-lookup"><span data-stu-id="21982-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="21982-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21982-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21982-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21982-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="21982-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21982-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21982-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21982-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




