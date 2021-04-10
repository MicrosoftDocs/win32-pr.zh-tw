---
description: 指定 XPS 列印工作是否在幕後處理或轉譯階段。
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: 'EPrintXPSJobOperation 列舉 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692903"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="18faa-103">EPrintXPSJobOperation 列舉</span><span class="sxs-lookup"><span data-stu-id="18faa-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="18faa-104">指定 XPS 列印工作是否在幕後處理或轉譯階段。</span><span class="sxs-lookup"><span data-stu-id="18faa-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="18faa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18faa-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="18faa-106">常數</span><span class="sxs-lookup"><span data-stu-id="18faa-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18faa-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span><span class="sxs-lookup"><span data-stu-id="18faa-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="18faa-108">XPS 工作為幕後處理。</span><span class="sxs-lookup"><span data-stu-id="18faa-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="18faa-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span><span class="sxs-lookup"><span data-stu-id="18faa-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="18faa-110">XPS 工作正在呈現。</span><span class="sxs-lookup"><span data-stu-id="18faa-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18faa-111">備註</span><span class="sxs-lookup"><span data-stu-id="18faa-111">Remarks</span></span>

<span data-ttu-id="18faa-112">這個列舉主要是用來做為 [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) 函式的參數。</span><span class="sxs-lookup"><span data-stu-id="18faa-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="18faa-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="18faa-113">Requirements</span></span>



| <span data-ttu-id="18faa-114">需求</span><span class="sxs-lookup"><span data-stu-id="18faa-114">Requirement</span></span> | <span data-ttu-id="18faa-115">值</span><span class="sxs-lookup"><span data-stu-id="18faa-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18faa-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18faa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18faa-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18faa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="18faa-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18faa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18faa-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18faa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18faa-120">標頭</span><span class="sxs-lookup"><span data-stu-id="18faa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="18faa-121"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="18faa-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




