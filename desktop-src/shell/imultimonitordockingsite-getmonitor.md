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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840639"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a><span data-ttu-id="d6c6b-103">IMultiMonitorDockingSite：： GetMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="d6c6b-103">IMultiMonitorDockingSite::GetMonitor method</span></span>

<span data-ttu-id="d6c6b-104">取得目前的預設監視器。</span><span class="sxs-lookup"><span data-stu-id="d6c6b-104">Gets the current default monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6c6b-105">Syntax</span></span>


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="d6c6b-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6c6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c6b-107">*punkSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c6b-108">類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="d6c6b-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="d6c6b-109">物件的指標，該物件會執行正在要求監視的 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) 介面。</span><span class="sxs-lookup"><span data-stu-id="d6c6b-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface for which the monitor is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="d6c6b-110">*phMon* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-110">*phMon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6c6b-111">類型： **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="d6c6b-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="d6c6b-112">當函式傳回時，會包含指向預設監視器控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="d6c6b-112">When the function returns, contains a pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c6b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6c6b-113">Return value</span></span>

<span data-ttu-id="d6c6b-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6c6b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d6c6b-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d6c6b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6c6b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d6c6b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c6b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6c6b-117">Requirements</span></span>



| <span data-ttu-id="d6c6b-118">需求</span><span class="sxs-lookup"><span data-stu-id="d6c6b-118">Requirement</span></span> | <span data-ttu-id="d6c6b-119">值</span><span class="sxs-lookup"><span data-stu-id="d6c6b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="d6c6b-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6c6b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c6b-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d6c6b-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6c6b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c6b-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6c6b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
