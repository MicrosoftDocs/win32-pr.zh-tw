---
description: 取得目前的預設監視器。
title: IMultiMonitorDockingSite：： GetMonitor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991695"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="24ee6-103">IMultiMonitorDockingSite：： GetMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="24ee6-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="24ee6-104">取得目前的預設監視器。</span><span class="sxs-lookup"><span data-stu-id="24ee6-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ee6-105">語法</span><span class="sxs-lookup"><span data-stu-id="24ee6-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="24ee6-106">參數</span><span class="sxs-lookup"><span data-stu-id="24ee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ee6-107">*punkSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ee6-108">類型： \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="24ee6-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="24ee6-109">物件的指標，該物件會執行正在要求監視的 [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)介面。</span><span class="sxs-lookup"><span data-stu-id="24ee6-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="24ee6-110">*phMon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24ee6-111">類型： \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="24ee6-111">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="24ee6-112">當函式傳回時，會包含指向預設監視器控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="24ee6-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ee6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="24ee6-113">Return value</span></span>

<span data-ttu-id="24ee6-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="24ee6-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="24ee6-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="24ee6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24ee6-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24ee6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ee6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="24ee6-117">Requirements</span></span>



| <span data-ttu-id="24ee6-118">需求</span><span class="sxs-lookup"><span data-stu-id="24ee6-118">Requirement</span></span> | <span data-ttu-id="24ee6-119">值</span><span class="sxs-lookup"><span data-stu-id="24ee6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="24ee6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24ee6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24ee6-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="24ee6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24ee6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24ee6-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24ee6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
