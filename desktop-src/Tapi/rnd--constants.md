---
description: 下列常數可能會傳回錯誤。
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: 'RND_ 常數 (Rnderr) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976046"
---
# <a name="rnd_-constants"></a><span data-ttu-id="e43b7-103">RND \_ 常數</span><span class="sxs-lookup"><span data-stu-id="e43b7-103">RND\_ Constants</span></span>

<span data-ttu-id="e43b7-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e43b7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e43b7-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e43b7-106">下列常數可能會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e43b7-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="e43b7-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND \_ 無效 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="e43b7-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e43b7-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="e43b7-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="e43b7-109">輸入的時間值無效。</span><span class="sxs-lookup"><span data-stu-id="e43b7-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e43b7-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND \_ Null \_ 伺服器 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="e43b7-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e43b7-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="e43b7-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="e43b7-112">伺服器名稱為 **Null**，可能是因為 [**ITConferenceBlob：： Init**](itconferenceblob-init.md) 尚未執行或未成功。</span><span class="sxs-lookup"><span data-stu-id="e43b7-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e43b7-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**\_已 \_ 連線的 RND**</span><span class="sxs-lookup"><span data-stu-id="e43b7-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e43b7-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="e43b7-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="e43b7-115">已呼叫 [**ITDirectory：： Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) 方法，但已經存在連接。</span><span class="sxs-lookup"><span data-stu-id="e43b7-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e43b7-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**\_未 \_ 連線的 RND**</span><span class="sxs-lookup"><span data-stu-id="e43b7-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e43b7-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="e43b7-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="e43b7-118">[**ITDirectory：： Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect)方法尚未呼叫或失敗。</span><span class="sxs-lookup"><span data-stu-id="e43b7-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e43b7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e43b7-119">Requirements</span></span>



| <span data-ttu-id="e43b7-120">需求</span><span class="sxs-lookup"><span data-stu-id="e43b7-120">Requirement</span></span> | <span data-ttu-id="e43b7-121">值</span><span class="sxs-lookup"><span data-stu-id="e43b7-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e43b7-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e43b7-122">TAPI version</span></span><br/> | <span data-ttu-id="e43b7-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e43b7-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="e43b7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e43b7-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e43b7-125"><dt>Rnderr。h</dt></span><span class="sxs-lookup"><span data-stu-id="e43b7-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




