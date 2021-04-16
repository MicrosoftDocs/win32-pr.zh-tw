---
title: 'WINBIO_EVENT 常數 (Winbio \_ 類型 .h) '
description: 指定要監視的服務提供者事件通知類型。
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508372"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="6e5ce-103">WINBIO \_ 事件常數</span><span class="sxs-lookup"><span data-stu-id="6e5ce-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="6e5ce-104">下列常數可以用在 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) 函式中，以指定要監視的服務提供者事件通知類型。</span><span class="sxs-lookup"><span data-stu-id="6e5ce-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="6e5ce-105">常數</span><span class="sxs-lookup"><span data-stu-id="6e5ce-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="6e5ce-106">描述</span><span class="sxs-lookup"><span data-stu-id="6e5ce-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="6e5ce-107"><dt>**WINBIO \_ 事件 \_ FP \_ 取消認領**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ce-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="6e5ce-108">感應器偵測到沒有應用程式要求的手指，或是目前有焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="6e5ce-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="6e5ce-109">Windows 生物特徵辨識架構會呼叫您的回呼函式，以表示已發生手指刷，但不會嘗試識別指紋。</span><span class="sxs-lookup"><span data-stu-id="6e5ce-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="6e5ce-110"><dt>**WINBIO \_ 事件 \_ FP \_ 取消認領 \_ 識別**</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ce-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="6e5ce-111">感應器偵測到沒有應用程式要求的手指，或是目前有焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="6e5ce-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="6e5ce-112">Windows 生物特徵辨識架構會嘗試識別指紋，並將該進程的結果傳遞給您的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="6e5ce-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="6e5ce-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e5ce-113">Requirements</span></span>



| <span data-ttu-id="6e5ce-114">需求</span><span class="sxs-lookup"><span data-stu-id="6e5ce-114">Requirement</span></span> | <span data-ttu-id="6e5ce-115">值</span><span class="sxs-lookup"><span data-stu-id="6e5ce-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5ce-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e5ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5ce-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e5ce-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6e5ce-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e5ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5ce-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e5ce-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6e5ce-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6e5ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e5ce-121"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6e5ce-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e5ce-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e5ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5ce-123">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="6e5ce-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





