---
title: 用戶端應用程式回呼函數
description: 兩種類型的回呼簽章。
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372491"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="cba5b-103">用戶端應用程式回呼函數</span><span class="sxs-lookup"><span data-stu-id="cba5b-103">Client Application Callback Functions</span></span>

<span data-ttu-id="cba5b-104">Windows 生物特徵辨識架構支援兩種類型的回呼簽章。</span><span class="sxs-lookup"><span data-stu-id="cba5b-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="cba5b-105">從 Windows 8 開始，支援下列回呼。</span><span class="sxs-lookup"><span data-stu-id="cba5b-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="cba5b-106">建議您針對所有新的應用程式執行此回呼。</span><span class="sxs-lookup"><span data-stu-id="cba5b-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="cba5b-107">不過，此回呼無法在 Windows 7 中使用。</span><span class="sxs-lookup"><span data-stu-id="cba5b-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="cba5b-108">回呼</span><span class="sxs-lookup"><span data-stu-id="cba5b-108">Callback</span></span>                                                                                     | <span data-ttu-id="cba5b-109">Description</span><span class="sxs-lookup"><span data-stu-id="cba5b-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cba5b-110">**PWINBIO \_ 非同步 \_ 完成 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="cba5b-111">通知用戶端應用程式，使用 [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) 或 [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) 啟動的非同步作業已完成。</span><span class="sxs-lookup"><span data-stu-id="cba5b-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="cba5b-112">下列回呼函數是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="cba5b-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="cba5b-113">我們建議您不要針對以 Windows 8 和更新版本的作業系統為目標的新應用程式執行這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="cba5b-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="cba5b-114">回呼</span><span class="sxs-lookup"><span data-stu-id="cba5b-114">Callback</span></span>                                                                                 | <span data-ttu-id="cba5b-115">Description</span><span class="sxs-lookup"><span data-stu-id="cba5b-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cba5b-116">**PWINBIO \_ CAPTURE \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="cba5b-117">傳回非同步 [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="cba5b-118">**PWINBIO \_ 註冊 \_ 捕獲 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="cba5b-119">傳回非同步 [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="cba5b-120">**PWINBIO \_ 事件 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="cba5b-121">傳回非同步 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="cba5b-122">**PWINBIO \_ 識別 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="cba5b-123">傳回非同步 [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="cba5b-124">**PWINBIO \_ 找出 \_ 感應器 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="cba5b-125">傳回非同步 [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="cba5b-126">**PWINBIO \_ 確認 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="cba5b-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="cba5b-127">傳回非同步 [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) 函數的結果。</span><span class="sxs-lookup"><span data-stu-id="cba5b-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="cba5b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="cba5b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba5b-129">用戶端應用程式參考</span><span class="sxs-lookup"><span data-stu-id="cba5b-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





