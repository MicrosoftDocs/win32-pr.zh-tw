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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841939"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a><span data-ttu-id="8c868-103">IMultiMonitorDockingSite：： SetMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="8c868-103">IMultiMonitorDockingSite::SetMonitor method</span></span>

<span data-ttu-id="8c868-104">變更用於多個監視器系統上停駐工具列的監視器。</span><span class="sxs-lookup"><span data-stu-id="8c868-104">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c868-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c868-105">Syntax</span></span>


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a><span data-ttu-id="8c868-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c868-107">*punkSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c868-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c868-108">類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="8c868-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="8c868-109">物件的指標，該物件會執行正在更改監視的 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) 介面。</span><span class="sxs-lookup"><span data-stu-id="8c868-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being altered.</span></span>

</dd> <dt>

<span data-ttu-id="8c868-110">*hMonNew* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c868-110">*hMonNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c868-111">類型： **HMONITOR**</span><span class="sxs-lookup"><span data-stu-id="8c868-111">Type: **HMONITOR**</span></span>

<span data-ttu-id="8c868-112">此監視器的控制碼，會取代現有的預設監視器。</span><span class="sxs-lookup"><span data-stu-id="8c868-112">A handle to the monitor that replaces the existing default monitor.</span></span>

</dd> <dt>

<span data-ttu-id="8c868-113">*phMonOld* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8c868-113">*phMonOld* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c868-114">類型： **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="8c868-114">Type: **HMONITOR\***</span></span>

<span data-ttu-id="8c868-115">當此函式傳回時，會包含先前預設監視器控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="8c868-115">When this function returns, contains a pointer to the previous default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c868-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c868-116">Return value</span></span>

<span data-ttu-id="8c868-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c868-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8c868-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8c868-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c868-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8c868-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c868-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c868-120">Requirements</span></span>



| <span data-ttu-id="8c868-121">需求</span><span class="sxs-lookup"><span data-stu-id="8c868-121">Requirement</span></span> | <span data-ttu-id="8c868-122">值</span><span class="sxs-lookup"><span data-stu-id="8c868-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="8c868-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c868-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8c868-124">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c868-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c868-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c868-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8c868-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c868-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
