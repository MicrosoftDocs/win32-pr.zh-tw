---
description: IAMErrorLog 介面提供在 DirectShow 編輯服務 (DES) 中進行錯誤記錄的回呼方法。DES 不會執行這個介面。
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: 'IAMErrorLog 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994652"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="0510f-103">IAMErrorLog 介面</span><span class="sxs-lookup"><span data-stu-id="0510f-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="0510f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0510f-104">\[Deprecated.</span></span> <span data-ttu-id="0510f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0510f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0510f-106">`IAMErrorLog`介面會在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中提供回呼方法，以進行錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="0510f-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="0510f-107">DES 不會執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="0510f-107">DES does not implement this interface.</span></span> <span data-ttu-id="0510f-108">若要執行錯誤記錄，請在您的應用程式中執行此介面，並在時間軸上呼叫 [**IAMSetErrorLog：:p \_ 錯誤**](iamseterrorlog-put-errorlog.md) 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="0510f-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="0510f-109">如果轉譯專案時發生錯誤，DES 會呼叫您的應用程式所執行的 [**IAMErrorLog：： LogError**](iamerrorlog-logerror.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0510f-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="0510f-110">只有當您使用 [**IRenderEngine**](irenderengine.md) 介面呈現專案時，DES 才會記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="0510f-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="0510f-111">例如，如果您將專案儲存為 DirectShow 篩選圖形 ( grf 格式) 並播放圖形檔案，則不會記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="0510f-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="0510f-112">如需使用此介面的詳細資訊，請參閱 [記錄錯誤](logging-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="0510f-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="0510f-113">成員</span><span class="sxs-lookup"><span data-stu-id="0510f-113">Members</span></span>

<span data-ttu-id="0510f-114">**IAMErrorLog** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="0510f-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0510f-115">**IAMErrorLog** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0510f-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="0510f-116">方法</span><span class="sxs-lookup"><span data-stu-id="0510f-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0510f-117">方法</span><span class="sxs-lookup"><span data-stu-id="0510f-117">Methods</span></span>

<span data-ttu-id="0510f-118">**IAMErrorLog** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0510f-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="0510f-119">方法</span><span class="sxs-lookup"><span data-stu-id="0510f-119">Method</span></span>                                   | <span data-ttu-id="0510f-120">描述</span><span class="sxs-lookup"><span data-stu-id="0510f-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="0510f-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="0510f-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="0510f-122">記錄錯誤。</span><span class="sxs-lookup"><span data-stu-id="0510f-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0510f-123">備註</span><span class="sxs-lookup"><span data-stu-id="0510f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0510f-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="0510f-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0510f-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0510f-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0510f-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="0510f-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0510f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0510f-127">Requirements</span></span>



| <span data-ttu-id="0510f-128">需求</span><span class="sxs-lookup"><span data-stu-id="0510f-128">Requirement</span></span> | <span data-ttu-id="0510f-129">值</span><span class="sxs-lookup"><span data-stu-id="0510f-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0510f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0510f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0510f-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0510f-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0510f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="0510f-132">Library</span></span><br/> | <dl> <span data-ttu-id="0510f-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0510f-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
