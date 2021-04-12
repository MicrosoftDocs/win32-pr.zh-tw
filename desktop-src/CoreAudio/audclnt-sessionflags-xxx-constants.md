---
description: AUDCLNT \_ SESSIONFLAGS \_ XXX 常數表示與資料流程相關聯之音訊會話的特性。
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: 'AUDCLNT_SESSIONFLAGS_XXX 常數 (Audiosessiontypes) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468548"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="54259-103">AUDCLNT \_ SESSIONFLAGS \_ XXX 常數</span><span class="sxs-lookup"><span data-stu-id="54259-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="54259-104">AUDCLNT \_ SESSIONFLAGS \_ XXX 常數表示與資料流程相關聯之音訊會話的特性。</span><span class="sxs-lookup"><span data-stu-id="54259-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="54259-105">用戶端可以透過 [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)方法的 *StreamFlags* 參數，在初始化資料流程期間指定這些選項。</span><span class="sxs-lookup"><span data-stu-id="54259-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="54259-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="54259-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="54259-107">Description</span><span class="sxs-lookup"><span data-stu-id="54259-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="54259-108"><dt>**AUDCLNT \_SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="54259-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="54259-109">當沒有相關聯的資料流程，並且擁有持有參考的會話控制物件時，會話就會過期。</span><span class="sxs-lookup"><span data-stu-id="54259-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="54259-110"><dt>**AUDCLNT \_SESSIONFLAGS \_ 顯示 \_ 隱藏**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="54259-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="54259-111">建立音訊會話時，音量控制項會隱藏在磁片區混音器使用者介面中。</span><span class="sxs-lookup"><span data-stu-id="54259-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="54259-112">如果與資料流程相關聯的會話已經存在， [**IAudioClient：： Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) 會開啟資料流程，磁片區控制項就會顯示在磁片區混音器中。</span><span class="sxs-lookup"><span data-stu-id="54259-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="54259-113"><dt> **AUDCLNT \_ SESSIONFLAGS \_ DISPLAY \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="54259-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="54259-114">在會話到期之後，音量控制會在磁片區混音器使用者介面中隱藏。</span><span class="sxs-lookup"><span data-stu-id="54259-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="54259-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="54259-115">Requirements</span></span>



| <span data-ttu-id="54259-116">需求</span><span class="sxs-lookup"><span data-stu-id="54259-116">Requirement</span></span> | <span data-ttu-id="54259-117">值</span><span class="sxs-lookup"><span data-stu-id="54259-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54259-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54259-118">Minimum supported client</span></span><br/> | <span data-ttu-id="54259-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54259-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="54259-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54259-120">Minimum supported server</span></span><br/> | <span data-ttu-id="54259-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54259-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54259-122">標頭</span><span class="sxs-lookup"><span data-stu-id="54259-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="54259-123"><dt>Audiosessiontypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="54259-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54259-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54259-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54259-125">核心音訊常數</span><span class="sxs-lookup"><span data-stu-id="54259-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="54259-126">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="54259-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




