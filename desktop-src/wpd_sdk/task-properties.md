---
description: Windows 可攜式裝置支援下列工作屬性。
ms.assetid: 9bd6c2e1-740a-453d-b390-120700af7c93
title: '工作屬性 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Task
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 829685ac3fa5737356c172ed9e66303b3d6115ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995682"
---
# <a name="task-properties"></a><span data-ttu-id="728bf-103">Task 屬性</span><span class="sxs-lookup"><span data-stu-id="728bf-103">Task Properties</span></span>

<span data-ttu-id="728bf-104">Windows 可攜式裝置支援下列工作屬性。</span><span class="sxs-lookup"><span data-stu-id="728bf-104">Windows Portable Devices supports the following task properties.</span></span>



| <span data-ttu-id="728bf-105">屬性</span><span class="sxs-lookup"><span data-stu-id="728bf-105">Property</span></span>                         | <span data-ttu-id="728bf-106">VarType</span><span class="sxs-lookup"><span data-stu-id="728bf-106">VarType</span></span>        | <span data-ttu-id="728bf-107">Description</span><span class="sxs-lookup"><span data-stu-id="728bf-107">Description</span></span>                                                                                 |
|----------------------------------|----------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="728bf-108">**WPD \_ 工作 \_ 擁有者**</span><span class="sxs-lookup"><span data-stu-id="728bf-108">**WPD\_TASK\_OWNER**</span></span>             | <span data-ttu-id="728bf-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="728bf-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="728bf-110">工作的擁有者。</span><span class="sxs-lookup"><span data-stu-id="728bf-110">The owner of the task.</span></span>                                                                      |
| <span data-ttu-id="728bf-111">**WPD \_ 工作 \_ \_ 完成百分比**</span><span class="sxs-lookup"><span data-stu-id="728bf-111">**WPD\_TASK\_PERCENT\_COMPLETE**</span></span> | <span data-ttu-id="728bf-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="728bf-112">**VT\_UI4**</span></span>    | <span data-ttu-id="728bf-113">介於0和100之間的數位，指定工作的完成程度。</span><span class="sxs-lookup"><span data-stu-id="728bf-113">A number between 0 and 100 that specifies how complete the task is.</span></span>                         |
| <span data-ttu-id="728bf-114">**WPD \_ 工作 \_ 提醒 \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="728bf-114">**WPD\_TASK\_REMINDER\_DATE**</span></span>    | <span data-ttu-id="728bf-115">**VT \_ 日期**</span><span class="sxs-lookup"><span data-stu-id="728bf-115">**VT\_DATE**</span></span>   | <span data-ttu-id="728bf-116">值，指定何時應該傳送提醒來執行工作（如果未完成）。</span><span class="sxs-lookup"><span data-stu-id="728bf-116">A value that specifies when a reminder should be sent to perform the task, if not complete.</span></span> |
| <span data-ttu-id="728bf-117">**WPD \_ 工作 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="728bf-117">**WPD\_TASK\_STATUS**</span></span>            | <span data-ttu-id="728bf-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="728bf-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="728bf-119">工作狀態的字串描述，例如「進行中」。</span><span class="sxs-lookup"><span data-stu-id="728bf-119">A string description of the status of the task, for example, "In Progress".</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="728bf-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="728bf-120">Requirements</span></span>



| <span data-ttu-id="728bf-121">需求</span><span class="sxs-lookup"><span data-stu-id="728bf-121">Requirement</span></span> | <span data-ttu-id="728bf-122">值</span><span class="sxs-lookup"><span data-stu-id="728bf-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="728bf-123">標頭</span><span class="sxs-lookup"><span data-stu-id="728bf-123">Header</span></span><br/> | <dl> <span data-ttu-id="728bf-124"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="728bf-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="728bf-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="728bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728bf-126">**WPD 屬性和屬性**</span><span class="sxs-lookup"><span data-stu-id="728bf-126">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




