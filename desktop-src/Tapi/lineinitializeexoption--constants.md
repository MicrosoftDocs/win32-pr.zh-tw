---
description: LINEINITIALIZEEXOPTION \_ 常數會指定初始化會話時要使用的事件通知機制。
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: 'LINEINITIALIZEEXOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991147"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="6836f-103">LINEINITIALIZEEXOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="6836f-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="6836f-104">**LINEINITIALIZEEXOPTION \_** 常數會指定初始化會話時要使用的事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="6836f-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="6836f-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="6836f-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6836f-106">應用程式想要使用呼叫中樞追蹤事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="6836f-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="6836f-107">這個常數只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6836f-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6836f-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="6836f-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6836f-109">應用程式想要使用完成埠事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="6836f-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="6836f-110">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6836f-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6836f-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="6836f-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6836f-112">應用程式想要使用事件處理常式事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="6836f-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="6836f-113">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6836f-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6836f-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="6836f-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6836f-115">應用程式想要使用隱藏的視窗事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="6836f-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="6836f-116">此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6836f-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6836f-117">備註</span><span class="sxs-lookup"><span data-stu-id="6836f-117">Remarks</span></span>

<span data-ttu-id="6836f-118">如需這些選項的詳細資訊，請參閱 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) 。</span><span class="sxs-lookup"><span data-stu-id="6836f-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="6836f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6836f-119">Requirements</span></span>



| <span data-ttu-id="6836f-120">需求</span><span class="sxs-lookup"><span data-stu-id="6836f-120">Requirement</span></span> | <span data-ttu-id="6836f-121">值</span><span class="sxs-lookup"><span data-stu-id="6836f-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6836f-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6836f-122">TAPI version</span></span><br/> | <span data-ttu-id="6836f-123">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6836f-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6836f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6836f-124">Header</span></span><br/>       | <dl> <span data-ttu-id="6836f-125"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="6836f-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




