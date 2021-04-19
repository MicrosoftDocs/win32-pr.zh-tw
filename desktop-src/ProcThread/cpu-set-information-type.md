---
description: 表示系統 \_ CPU \_ 集資訊結構中的資訊類型 \_ 。
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: 'CPU_SET_INFORMATION_TYPE 列舉 (Processthreadapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975091"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="a399c-103">CPU \_ 集 \_ 資訊 \_ 類型列舉</span><span class="sxs-lookup"><span data-stu-id="a399c-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="a399c-104">表示 [**系統 \_ CPU \_ 集 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) 結構中的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="a399c-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a399c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a399c-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="a399c-106">常數</span><span class="sxs-lookup"><span data-stu-id="a399c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a399c-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span><span class="sxs-lookup"><span data-stu-id="a399c-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="a399c-108">此結構包含 CPU 集資訊。</span><span class="sxs-lookup"><span data-stu-id="a399c-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a399c-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="a399c-109">Requirements</span></span>



| <span data-ttu-id="a399c-110">需求</span><span class="sxs-lookup"><span data-stu-id="a399c-110">Requirement</span></span> | <span data-ttu-id="a399c-111">值</span><span class="sxs-lookup"><span data-stu-id="a399c-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a399c-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a399c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a399c-113">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a399c-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="a399c-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a399c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a399c-115">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a399c-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a399c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a399c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a399c-117"><dt>Processthreadsapi (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a399c-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




