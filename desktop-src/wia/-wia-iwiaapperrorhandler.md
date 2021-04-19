---
description: IWiaAppErrorHandler 介面可讓應用程式在資料傳輸期間顯示錯誤的 windows () 使用者可以從中選擇是否要繼續、取消或中止傳送。
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: 'IWiaAppErrorHandler 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971807"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="d3146-103">IWiaAppErrorHandler 介面</span><span class="sxs-lookup"><span data-stu-id="d3146-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="d3146-104">**IWiaAppErrorHandler** 介面可讓應用程式在資料傳輸期間顯示錯誤的 windows () 使用者可以從中選擇是否要繼續、取消或中止傳送。</span><span class="sxs-lookup"><span data-stu-id="d3146-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="d3146-105">成員</span><span class="sxs-lookup"><span data-stu-id="d3146-105">Members</span></span>

<span data-ttu-id="d3146-106">**IWiaAppErrorHandler** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="d3146-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d3146-107">**IWiaAppErrorHandler** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d3146-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="d3146-108">方法</span><span class="sxs-lookup"><span data-stu-id="d3146-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3146-109">方法</span><span class="sxs-lookup"><span data-stu-id="d3146-109">Methods</span></span>

<span data-ttu-id="d3146-110">**IWiaAppErrorHandler** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d3146-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="d3146-111">方法</span><span class="sxs-lookup"><span data-stu-id="d3146-111">Method</span></span>                                                        | <span data-ttu-id="d3146-112">描述</span><span class="sxs-lookup"><span data-stu-id="d3146-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3146-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="d3146-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="d3146-114">取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。</span><span class="sxs-lookup"><span data-stu-id="d3146-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="d3146-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="d3146-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="d3146-116">處理影像資料傳輸期間的裝置狀態和錯誤訊息，並向使用者顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="d3146-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="d3146-117">備註</span><span class="sxs-lookup"><span data-stu-id="d3146-117">Remarks</span></span>

<span data-ttu-id="d3146-118">處理此介面的錯誤處理（或回呼）物件會傳遞至 [**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md) 和 [**IWiaTransfer：： Upload**](-wia-iwiatransfer-upload.md)。</span><span class="sxs-lookup"><span data-stu-id="d3146-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="d3146-119">此介面並非設計用來處理在影像資料傳輸之外發生的錯誤，例如，取得或設定裝置屬性或 unreturned 回呼至驅動程式時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d3146-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="d3146-120">驅動程式錯誤處理常式應該執行 [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)，而不是 **IWiaAppErrorHandler**。</span><span class="sxs-lookup"><span data-stu-id="d3146-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="d3146-121">執行這個介面的物件也應該執行 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md)。</span><span class="sxs-lookup"><span data-stu-id="d3146-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="d3146-122">如果您想要驅動程式錯誤處理常式和預設錯誤處理常式來顯示錯誤訊息視窗，但您不想要為應用程式建立完整的錯誤處理常式，請執行這個介面，並同時執行 [**IWiaAppErrorHandler：： ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) 方法，以傳回 \_ 未處理的 WIA 狀態 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="d3146-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3146-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3146-123">Requirements</span></span>



| <span data-ttu-id="d3146-124">需求</span><span class="sxs-lookup"><span data-stu-id="d3146-124">Requirement</span></span> | <span data-ttu-id="d3146-125">值</span><span class="sxs-lookup"><span data-stu-id="d3146-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3146-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3146-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3146-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3146-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d3146-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3146-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3146-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3146-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3146-130">標頭</span><span class="sxs-lookup"><span data-stu-id="d3146-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3146-131"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="d3146-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3146-132">Idl</span><span class="sxs-lookup"><span data-stu-id="d3146-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3146-133"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3146-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
