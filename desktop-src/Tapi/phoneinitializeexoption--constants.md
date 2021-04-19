---
description: PHONEINITIALIZEEXOPTION \_ 常數會指定初始化會話時要使用的事件通知機制。
ms.assetid: 7d8b122d-bebe-4904-abc8-d680b0899e25
title: 'PHONEINITIALIZEEXOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023f6801f65910bedf7d2637079694b4c6b6d85e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993252"
---
# <a name="phoneinitializeexoption_-constants"></a><span data-ttu-id="71b46-103">PHONEINITIALIZEEXOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="71b46-103">PHONEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="71b46-104">**PHONEINITIALIZEEXOPTION \_** 常數會指定初始化會話時要使用的事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="71b46-104">The **PHONEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="71b46-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="71b46-105"><span id="PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="phoneinitializeexoption_usecompletionport"></span>**PHONEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71b46-106">應用程式想要使用完成埠事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="71b46-106">The application desires to use the Completion Port event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71b46-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="71b46-107"><span id="PHONEINITIALIZEEXOPTION_USEEVENT"></span><span id="phoneinitializeexoption_useevent"></span>**PHONEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71b46-108">應用程式想要使用事件處理常式事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="71b46-108">The application desires to use the Event Handle event notification mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="71b46-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="71b46-109"><span id="PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="phoneinitializeexoption_usehiddenwindow"></span>**PHONEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="71b46-110">應用程式想要使用隱藏的視窗事件通知機制。</span><span class="sxs-lookup"><span data-stu-id="71b46-110">The application desires to use the Hidden Window event notification mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71b46-111">備註</span><span class="sxs-lookup"><span data-stu-id="71b46-111">Remarks</span></span>

<span data-ttu-id="71b46-112">如需這些選項的詳細資訊，請參閱 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) 。</span><span class="sxs-lookup"><span data-stu-id="71b46-112">See [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b46-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="71b46-113">Requirements</span></span>



| <span data-ttu-id="71b46-114">需求</span><span class="sxs-lookup"><span data-stu-id="71b46-114">Requirement</span></span> | <span data-ttu-id="71b46-115">值</span><span class="sxs-lookup"><span data-stu-id="71b46-115">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71b46-116">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="71b46-116">TAPI version</span></span><br/> | <span data-ttu-id="71b46-117">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="71b46-117">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="71b46-118">標頭</span><span class="sxs-lookup"><span data-stu-id="71b46-118">Header</span></span><br/>       | <dl> <span data-ttu-id="71b46-119"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="71b46-119"><dt>Tapi.h</dt></span></span> </dl> |



 

 




