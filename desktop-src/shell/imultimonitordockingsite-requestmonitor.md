---
description: 確認監視器正在使用中且可供使用。
title: IMultiMonitorDockingSite：： RequestMonitor 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841969"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a><span data-ttu-id="f1636-103">IMultiMonitorDockingSite：： RequestMonitor 方法</span><span class="sxs-lookup"><span data-stu-id="f1636-103">IMultiMonitorDockingSite::RequestMonitor method</span></span>

<span data-ttu-id="f1636-104">確認監視器正在使用中且可供使用。</span><span class="sxs-lookup"><span data-stu-id="f1636-104">Verifies that the monitor is active and available.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1636-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1636-105">Syntax</span></span>


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a><span data-ttu-id="f1636-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1636-107">*punkSrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1636-107">*punkSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1636-108">類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="f1636-108">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="f1636-109">執行 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) 介面之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f1636-109">A pointer to the object implementing the [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f1636-110">*phMon* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1636-110">*phMon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1636-111">類型： **HMONITOR \***</span><span class="sxs-lookup"><span data-stu-id="f1636-111">Type: **HMONITOR\***</span></span>

<span data-ttu-id="f1636-112">預設監視之控制碼的指標。</span><span class="sxs-lookup"><span data-stu-id="f1636-112">A pointer to the default monitor's handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1636-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1636-113">Return value</span></span>

<span data-ttu-id="f1636-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f1636-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f1636-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f1636-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1636-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f1636-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1636-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1636-117">Requirements</span></span>



| <span data-ttu-id="f1636-118">需求</span><span class="sxs-lookup"><span data-stu-id="f1636-118">Requirement</span></span> | <span data-ttu-id="f1636-119">值</span><span class="sxs-lookup"><span data-stu-id="f1636-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="f1636-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1636-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f1636-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1636-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1636-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1636-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f1636-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1636-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
