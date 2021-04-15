---
description: 指出正在執行之專家的目前狀態。
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: 'EXPERTSTATUS 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510981"
---
# <a name="expertstatus-structure"></a><span data-ttu-id="ced06-103">EXPERTSTATUS 結構</span><span class="sxs-lookup"><span data-stu-id="ced06-103">EXPERTSTATUS structure</span></span>

<span data-ttu-id="ced06-104">**EXPERTSTATUS** 結構指出正在執行之專家的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="ced06-104">The **EXPERTSTATUS** structure indicates the current status of a running expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced06-105">語法</span><span class="sxs-lookup"><span data-stu-id="ced06-105">Syntax</span></span>


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a><span data-ttu-id="ced06-106">成員</span><span class="sxs-lookup"><span data-stu-id="ced06-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ced06-107">**狀態**</span><span class="sxs-lookup"><span data-stu-id="ced06-107">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="ced06-108">[**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md)列舉所定義的目前專家狀態值。</span><span class="sxs-lookup"><span data-stu-id="ced06-108">Current expert status value defined by the [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-109">**狀態值**</span><span class="sxs-lookup"><span data-stu-id="ced06-109">**SubStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ced06-110">子狀態值。</span><span class="sxs-lookup"><span data-stu-id="ced06-110">Sub-status value.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-111">**PercentDone**</span><span class="sxs-lookup"><span data-stu-id="ced06-111">**PercentDone**</span></span>
</dt> <dd>

<span data-ttu-id="ced06-112">已完成的網路資料專家分析完成百分比。</span><span class="sxs-lookup"><span data-stu-id="ced06-112">Percentage completion of the expert analysis of network data.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-113">**Frame**</span><span class="sxs-lookup"><span data-stu-id="ced06-113">**Frame**</span></span>
</dt> <dd>

<span data-ttu-id="ced06-114">畫面格編號。</span><span class="sxs-lookup"><span data-stu-id="ced06-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="ced06-115">**szStatusText**</span><span class="sxs-lookup"><span data-stu-id="ced06-115">**szStatusText**</span></span>
</dt> <dd>

<span data-ttu-id="ced06-116">描述專家狀態的文字。</span><span class="sxs-lookup"><span data-stu-id="ced06-116">Text that describes the expert status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ced06-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ced06-117">Requirements</span></span>



| <span data-ttu-id="ced06-118">需求</span><span class="sxs-lookup"><span data-stu-id="ced06-118">Requirement</span></span> | <span data-ttu-id="ced06-119">值</span><span class="sxs-lookup"><span data-stu-id="ced06-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ced06-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ced06-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ced06-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ced06-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ced06-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ced06-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ced06-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ced06-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ced06-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ced06-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ced06-125"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="ced06-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




