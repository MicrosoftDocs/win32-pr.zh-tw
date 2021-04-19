---
description: IAMSetErrorLog 介面會設定或抓取 DirectShow 編輯服務 (DES) 中的錯誤記錄檔。
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: 'IAMSetErrorLog 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976025"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="58ce6-103">IAMSetErrorLog 介面</span><span class="sxs-lookup"><span data-stu-id="58ce6-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="58ce6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="58ce6-104">\[Deprecated.</span></span> <span data-ttu-id="58ce6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="58ce6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58ce6-106">`IAMSetErrorLog`介面會設定或抓取[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="58ce6-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="58ce6-107">時間軸物件會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="58ce6-107">The timeline object implements this interface.</span></span> <span data-ttu-id="58ce6-108">應用程式可以使用這個介面來記錄執行時間的轉譯錯誤。</span><span class="sxs-lookup"><span data-stu-id="58ce6-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="58ce6-109">在您的應用程式中執行 [**IAMErrorLog**](iamerrorlog.md) 介面，然後在時間軸上呼叫 [**IAMSetErrorLog：:p 的 \_ 錯誤**](iamseterrorlog-put-errorlog.md) 記錄檔方法。</span><span class="sxs-lookup"><span data-stu-id="58ce6-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="58ce6-110">如需使用此介面的詳細資訊，請參閱 [記錄錯誤](logging-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="58ce6-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="58ce6-111">成員</span><span class="sxs-lookup"><span data-stu-id="58ce6-111">Members</span></span>

<span data-ttu-id="58ce6-112">**IAMSetErrorLog** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="58ce6-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="58ce6-113">**IAMSetErrorLog** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="58ce6-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="58ce6-114">方法</span><span class="sxs-lookup"><span data-stu-id="58ce6-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58ce6-115">方法</span><span class="sxs-lookup"><span data-stu-id="58ce6-115">Methods</span></span>

<span data-ttu-id="58ce6-116">**IAMSetErrorLog** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="58ce6-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="58ce6-117">方法</span><span class="sxs-lookup"><span data-stu-id="58ce6-117">Method</span></span>                                               | <span data-ttu-id="58ce6-118">描述</span><span class="sxs-lookup"><span data-stu-id="58ce6-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="58ce6-119">**取得 \_ 錯誤記錄檔**</span><span class="sxs-lookup"><span data-stu-id="58ce6-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="58ce6-120">抓取這個物件目前的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="58ce6-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="58ce6-121">**put \_ 錯誤記錄檔**</span><span class="sxs-lookup"><span data-stu-id="58ce6-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="58ce6-122">指定物件的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="58ce6-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="58ce6-123">備註</span><span class="sxs-lookup"><span data-stu-id="58ce6-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58ce6-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="58ce6-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58ce6-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="58ce6-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58ce6-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="58ce6-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58ce6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="58ce6-127">Requirements</span></span>



| <span data-ttu-id="58ce6-128">需求</span><span class="sxs-lookup"><span data-stu-id="58ce6-128">Requirement</span></span> | <span data-ttu-id="58ce6-129">值</span><span class="sxs-lookup"><span data-stu-id="58ce6-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ce6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="58ce6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="58ce6-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="58ce6-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58ce6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="58ce6-132">Library</span></span><br/> | <dl> <span data-ttu-id="58ce6-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ce6-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
