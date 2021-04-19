---
description: 取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'IWiaAppErrorHandler：： GetWindow 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979163"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a><span data-ttu-id="00fad-103">IWiaAppErrorHandler：： GetWindow 方法</span><span class="sxs-lookup"><span data-stu-id="00fad-103">IWiaAppErrorHandler::GetWindow method</span></span>

<span data-ttu-id="00fad-104">取得對話方塊的控制碼，此控制碼會顯示錯誤訊息，並提供一或多個按鈕來繼續、取消或中止應用程式。</span><span class="sxs-lookup"><span data-stu-id="00fad-104">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fad-105">語法</span><span class="sxs-lookup"><span data-stu-id="00fad-105">Syntax</span></span>


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a><span data-ttu-id="00fad-106">參數</span><span class="sxs-lookup"><span data-stu-id="00fad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fad-107">*phwnd* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00fad-107">*phwnd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00fad-108">類型： \**HWND \** _</span><span class="sxs-lookup"><span data-stu-id="00fad-108">Type: \**HWND\** _</span></span>

<span data-ttu-id="00fad-109">應用程式錯誤處理常式所使用的 HWND、驅動程式錯誤處理常式，以及裝置訊息對話方塊的預設錯誤處理常式 (錯誤和資訊性) 。</span><span class="sxs-lookup"><span data-stu-id="00fad-109">HWND used by the application error handler, the driver error handler, and the default error handler for device message dialog boxes (both error and informational).</span></span> <span data-ttu-id="00fad-110">輸出值可能是 _ \* Null \* \*。</span><span class="sxs-lookup"><span data-stu-id="00fad-110">The output value may be _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fad-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="00fad-111">Return value</span></span>

<span data-ttu-id="00fad-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00fad-112">Type: **HRESULT**</span></span>

<span data-ttu-id="00fad-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="00fad-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00fad-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00fad-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00fad-115">備註</span><span class="sxs-lookup"><span data-stu-id="00fad-115">Remarks</span></span>

<span data-ttu-id="00fad-116">*phwnd* 指向 Windows 映像取得 (WIA) 2.0 Proxy 傳遞至 [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) 的視窗。</span><span class="sxs-lookup"><span data-stu-id="00fad-116">*phwnd* points to the window passed into [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) by the Windows Image Acquisition (WIA) 2.0 Proxy.</span></span> <span data-ttu-id="00fad-117">此視窗在資料傳輸期間必須保持有效。</span><span class="sxs-lookup"><span data-stu-id="00fad-117">This window must remain valid for the duration of the data transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="00fad-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="00fad-118">Requirements</span></span>



| <span data-ttu-id="00fad-119">需求</span><span class="sxs-lookup"><span data-stu-id="00fad-119">Requirement</span></span> | <span data-ttu-id="00fad-120">值</span><span class="sxs-lookup"><span data-stu-id="00fad-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00fad-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00fad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00fad-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00fad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00fad-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00fad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00fad-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00fad-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00fad-125">標頭</span><span class="sxs-lookup"><span data-stu-id="00fad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00fad-126"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="00fad-126"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="00fad-127">Idl</span><span class="sxs-lookup"><span data-stu-id="00fad-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00fad-128"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="00fad-128"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="00fad-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="00fad-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="00fad-130"><dt>Wiaguid .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00fad-130"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




