---
title: 'Windows 事件記錄檔資料類型 (\System32\winevt\logs\application.evtx .h) '
description: Windows 事件記錄檔會定義下列資料類型
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685879"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="4a556-106">Windows 事件記錄檔資料類型</span><span class="sxs-lookup"><span data-stu-id="4a556-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="4a556-107">Windows 事件記錄檔會定義下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="4a556-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="4a556-108">**.EVT \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="4a556-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="4a556-109">Windows 事件記錄檔物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a556-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="4a556-110">**PEVT \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="4a556-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="4a556-111">Windows 事件記錄檔物件的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="4a556-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="4a556-112">**.EVT \_ 物件 \_ 陣列 \_ 屬性 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="4a556-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="4a556-113">Windows 事件記錄檔物件陣列的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a556-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a556-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a556-114">Requirements</span></span>



| <span data-ttu-id="4a556-115">需求</span><span class="sxs-lookup"><span data-stu-id="4a556-115">Requirement</span></span> | <span data-ttu-id="4a556-116">值</span><span class="sxs-lookup"><span data-stu-id="4a556-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4a556-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a556-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a556-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a556-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a556-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a556-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a556-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a556-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4a556-121">標頭</span><span class="sxs-lookup"><span data-stu-id="4a556-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a556-122"><dt>\System32\winevt\logs\application.evtx。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a556-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





