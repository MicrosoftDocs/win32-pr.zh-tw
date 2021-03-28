---
description: 變更用於多個監視器系統上停駐工具列的監視器。
title: IMultiMonitorDockingSite：： SetMonitor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991823"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="1634e-103">IMultiMonitorDockingSite：： SetMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="1634e-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="1634e-104">變更用於多個監視器系統上停駐工具列的監視器。</span><span class="sxs-lookup"><span data-stu-id="1634e-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1634e-105">語法</span><span class="sxs-lookup"><span data-stu-id="1634e-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="1634e-106">參數</span><span class="sxs-lookup"><span data-stu-id="1634e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1634e-107">*punkSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1634e-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1634e-108">類型： \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="1634e-108">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="1634e-109">物件的指標，該物件會執行正在更改監視的 [_ *IDockingWindow* \*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)介面。</span><span class="sxs-lookup"><span data-stu-id="1634e-109">A pointer to the object implementing the [_ *IDockingWindow*\*](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-110">*hMonNew* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1634e-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1634e-111">類型： **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="1634e-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="1634e-112">此監視器的控制碼，會取代現有的預設監視器。</span><span class="sxs-lookup"><span data-stu-id="1634e-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-113">*phMonOld* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1634e-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1634e-114">類型： \**HMONITOR \** _</span><span class="sxs-lookup"><span data-stu-id="1634e-114">Type: \**HMONITOR\** _</span></span>

<span data-ttu-id="1634e-115">當此函式傳回時，會包含先前預設監視器控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="1634e-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1634e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1634e-116">Return value</span></span>

<span data-ttu-id="1634e-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1634e-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1634e-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1634e-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1634e-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1634e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1634e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1634e-120">Requirements</span></span>



| <span data-ttu-id="1634e-121">需求</span><span class="sxs-lookup"><span data-stu-id="1634e-121">Requirement</span></span> | <span data-ttu-id="1634e-122">值</span><span class="sxs-lookup"><span data-stu-id="1634e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="1634e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1634e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1634e-124">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1634e-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1634e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1634e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1634e-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1634e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
