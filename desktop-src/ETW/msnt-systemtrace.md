---
description: 衍生所有系統事件追蹤類別的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972281"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="93043-104">MSNT \_ SystemTrace 類別</span><span class="sxs-lookup"><span data-stu-id="93043-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="93043-105">衍生所有系統事件追蹤類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="93043-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="93043-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="93043-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="93043-107">語法</span><span class="sxs-lookup"><span data-stu-id="93043-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="93043-108">成員</span><span class="sxs-lookup"><span data-stu-id="93043-108">Members</span></span>

<span data-ttu-id="93043-109">**MSNT \_ SystemTrace** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93043-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="93043-110">屬性</span><span class="sxs-lookup"><span data-stu-id="93043-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93043-111">屬性</span><span class="sxs-lookup"><span data-stu-id="93043-111">Properties</span></span>

<span data-ttu-id="93043-112">**MSNT \_ SystemTrace** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93043-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93043-113">**旗標**</span><span class="sxs-lookup"><span data-stu-id="93043-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93043-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93043-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93043-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="93043-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93043-116">限定詞： DefineValues {「事件追蹤旗標進程」、「事件追蹤旗標執行緒」、「事件追蹤旗標映射載入」、「事件追蹤旗標進程計數器」、「事件追蹤旗標」、「事件追蹤旗標 DPC」、「事件追蹤 **\_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 旗標中斷」 \_ \_ \_ 、」 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 事件 \_ 追蹤旗標 \_ \_ SYSTEMCALL "、「事件追蹤旗標磁片 io」、「事件追蹤旗標磁片檔案 \_ \_ \_ \_ io \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_**」、「事件追蹤旗標磁片 IO 初始化」、「事件追蹤旗標發送器」、「事件追蹤旗標記憶體分頁錯誤」、「事件追蹤旗標記憶體硬錯誤」、「事件追蹤旗標網路 TCPIP」、事件追蹤旗標登錄」、「事件追蹤旗標 ALPC」、「事件追蹤旗標分割 IO」、「事件追蹤旗標驅動程式」、「事件追蹤旗標設定檔」、「事件追蹤旗標檔案 IO」、「事件追蹤」旗標檔案 IO INIT"}、 **ValueMap {"0x00000001"、"0x00000002"、"0x00000004"、"0x00000008"、"0x00000010"、"0x00000020"、"0x00000040"、"0x00000080"、"0x00000100"、"0x00000200"、"0x00000400"、"0x00000800"、"0x00001000"、"0x00002000"、"0x00004000"、"0x00010000"、"0x00020000"、"0x00100000"、"0x00200000"、"0x00800000"、"0x01000000"、"0x02000000"、"0x04000000"}**</span><span class="sxs-lookup"><span data-stu-id="93043-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="93043-117">啟用旗標，指出已啟用的核心提供者。</span><span class="sxs-lookup"><span data-stu-id="93043-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93043-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="93043-118">Requirements</span></span>



| <span data-ttu-id="93043-119">需求</span><span class="sxs-lookup"><span data-stu-id="93043-119">Requirement</span></span> | <span data-ttu-id="93043-120">值</span><span class="sxs-lookup"><span data-stu-id="93043-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="93043-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93043-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93043-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93043-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93043-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93043-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93043-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93043-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




