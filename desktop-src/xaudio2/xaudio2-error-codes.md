---
description: XAudio2 XAudio2 方法所傳回的特定錯誤碼。
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: 'XAudio2 錯誤碼 (Xaudio2) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987919"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="ddbd3-103">XAudio2 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ddbd3-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="ddbd3-104">XAudio2 XAudio2 方法所傳回的特定錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ddbd3-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="ddbd3-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ddbd3-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="ddbd3-106">Description</span><span class="sxs-lookup"><span data-stu-id="ddbd3-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="ddbd3-107"><dt>**XAUDIO2 \_E \_ 不正確 \_ 呼叫**</dt> <dt>0x88960001</dt></span><span class="sxs-lookup"><span data-stu-id="ddbd3-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="ddbd3-108">XAudio2 針對某些 API 使用錯誤所傳回的錯誤 (不正確呼叫，以及在執行時間應由標題處理的) 。</span><span class="sxs-lookup"><span data-stu-id="ddbd3-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="ddbd3-109"> (完全肇因的 API 使用錯誤（例如不正確參數），會導致在零售組建中的偵測組建和未定義行為發生判斷提示，因此未定義任何錯誤碼。 ) </span><span class="sxs-lookup"><span data-stu-id="ddbd3-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="ddbd3-110"><dt>**XAUDIO2 \_E \_ XMA \_ 解碼器 \_ ERROR**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="ddbd3-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="ddbd3-111">Xbox 360 XMA 硬體遭受無法復原的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ddbd3-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="ddbd3-112"><dt>**XAUDIO2 \_E \_ XAPO \_ 建立 \_ 失敗**</dt> <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="ddbd3-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="ddbd3-113">無法具現化效果。</span><span class="sxs-lookup"><span data-stu-id="ddbd3-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="ddbd3-114"><dt>**XAUDIO2 \_E \_ 裝置 \_ 失效**</dt> <dt>0x88960004</dt></span><span class="sxs-lookup"><span data-stu-id="ddbd3-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="ddbd3-115">音訊裝置無法透過插即用或其他事件來使用。</span><span class="sxs-lookup"><span data-stu-id="ddbd3-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="ddbd3-116">備註</span><span class="sxs-lookup"><span data-stu-id="ddbd3-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ddbd3-117">平台需求</span><span class="sxs-lookup"><span data-stu-id="ddbd3-117">Platform Requirements</span></span>

<span data-ttu-id="ddbd3-118">Windows 10 (XAudio 2.9) ;Windows 8、Windows Phone 8 (XAudio 2.8) ;DirectX SDK (XAudio 2.7) </span><span class="sxs-lookup"><span data-stu-id="ddbd3-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbd3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ddbd3-119">Requirements</span></span>



| <span data-ttu-id="ddbd3-120">需求</span><span class="sxs-lookup"><span data-stu-id="ddbd3-120">Requirement</span></span> | <span data-ttu-id="ddbd3-121">值</span><span class="sxs-lookup"><span data-stu-id="ddbd3-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbd3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ddbd3-122">Header</span></span><br/> | <dl> <span data-ttu-id="ddbd3-123"><dt>Xaudio2。h</dt></span><span class="sxs-lookup"><span data-stu-id="ddbd3-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbd3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddbd3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbd3-125">XAudio2：：常數</span><span class="sxs-lookup"><span data-stu-id="ddbd3-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 




