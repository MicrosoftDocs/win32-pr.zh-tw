---
description: 代表所有物件管理員事件追蹤類別衍生來源的父類別。
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: ObTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693748"
---
# <a name="obtrace-class"></a><span data-ttu-id="1de98-103">ObTrace 類別</span><span class="sxs-lookup"><span data-stu-id="1de98-103">ObTrace class</span></span>

<span data-ttu-id="1de98-104">代表所有物件管理員事件追蹤類別衍生來源的父類別。</span><span class="sxs-lookup"><span data-stu-id="1de98-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="1de98-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1de98-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de98-106">語法</span><span class="sxs-lookup"><span data-stu-id="1de98-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1de98-107">成員</span><span class="sxs-lookup"><span data-stu-id="1de98-107">Members</span></span>

<span data-ttu-id="1de98-108">**ObTrace** 類別不會定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="1de98-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1de98-109">備註</span><span class="sxs-lookup"><span data-stu-id="1de98-109">Remarks</span></span>

<span data-ttu-id="1de98-110">若要啟用物件管理員事件追蹤，請呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函數，並將 *InformationClass* 參數等於 [**追蹤 \_ 資訊 \_ 類別**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) 列舉值 **TraceSystemTraceEnableFlagsInfo** ，且 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的 **EnableFlags** 成員等於效能 **\_ OB \_ 控制碼** (0x80000040) 。</span><span class="sxs-lookup"><span data-stu-id="1de98-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="1de98-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1de98-111">Requirements</span></span>



| <span data-ttu-id="1de98-112">需求</span><span class="sxs-lookup"><span data-stu-id="1de98-112">Requirement</span></span> | <span data-ttu-id="1de98-113">值</span><span class="sxs-lookup"><span data-stu-id="1de98-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1de98-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1de98-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1de98-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de98-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1de98-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1de98-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1de98-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de98-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1de98-118">MOF</span><span class="sxs-lookup"><span data-stu-id="1de98-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1de98-119"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="1de98-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
