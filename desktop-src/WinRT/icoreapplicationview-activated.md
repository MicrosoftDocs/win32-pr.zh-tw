---
description: 在啟用 Windows Store 應用程式時發生。
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'ICoreApplicationView：：啟動的事件 (ApplicationModel) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191350"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="eb97f-103">ICoreApplicationView：：已啟用事件</span><span class="sxs-lookup"><span data-stu-id="eb97f-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="eb97f-104">在啟用 Windows Store 應用程式時發生。</span><span class="sxs-lookup"><span data-stu-id="eb97f-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb97f-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb97f-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="eb97f-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb97f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb97f-107">*處理常式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb97f-107">*handler* \[in\]</span></span>
<span data-ttu-id="eb97f-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eb97f-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="eb97f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb97f-109">Return value</span></span>

<span data-ttu-id="eb97f-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eb97f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb97f-111">備註</span><span class="sxs-lookup"><span data-stu-id="eb97f-111">Remarks</span></span>

<span data-ttu-id="eb97f-112">請勿從 *處理常式* 內呼叫 [**Exit**](/previous-versions//hh438368(v=vs.85))方法。</span><span class="sxs-lookup"><span data-stu-id="eb97f-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb97f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb97f-113">Requirements</span></span>



| <span data-ttu-id="eb97f-114">需求</span><span class="sxs-lookup"><span data-stu-id="eb97f-114">Requirement</span></span> | <span data-ttu-id="eb97f-115">值</span><span class="sxs-lookup"><span data-stu-id="eb97f-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb97f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb97f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eb97f-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eb97f-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="eb97f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb97f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eb97f-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb97f-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="eb97f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="eb97f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb97f-121"><dt>ApplicationModel Core。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb97f-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb97f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="eb97f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb97f-123"><dt>ApplicationModel。</dt></span><span class="sxs-lookup"><span data-stu-id="eb97f-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
