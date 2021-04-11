---
description: PKEY \_ AudioEndpoint \_ Disable \_ SysFx 屬性會指定是否在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: 'PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111193"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a><span data-ttu-id="bea34-103">PKEY \_ AudioEndpoint \_ Disable \_ SysFx</span><span class="sxs-lookup"><span data-stu-id="bea34-103">PKEY\_AudioEndpoint\_Disable\_SysFx</span></span>

<span data-ttu-id="bea34-104">**PKEY \_ AudioEndpoint \_ Disable \_ SysFx** 屬性會指定是否在流入或流出音訊端點裝置的共用模式資料流程中啟用系統效果。</span><span class="sxs-lookup"><span data-stu-id="bea34-104">The **PKEY\_AudioEndpoint\_Disable\_SysFx** property specifies whether system effects are enabled in the shared-mode stream that flows to or from the audio endpoint device.</span></span>

<span data-ttu-id="bea34-105">系統效果會實作為音訊處理物件， (可以插入音訊串流中的) 。</span><span class="sxs-lookup"><span data-stu-id="bea34-105">System effects are implemented as audio processing objects (APOs) that can be inserted into an audio stream.</span></span> <span data-ttu-id="bea34-106">是執行音訊處理功能的軟體模組，例如音量控制和格式轉換。</span><span class="sxs-lookup"><span data-stu-id="bea34-106">APOs are software modules that perform audio processing functions such as volume control and format conversion.</span></span> <span data-ttu-id="bea34-107">停用端點裝置的系統效果，可讓相關聯的串流通過未修改的。</span><span class="sxs-lookup"><span data-stu-id="bea34-107">Disabling the system effects for an endpoint device enables the associated stream to pass through the APOs unmodified.</span></span>

<span data-ttu-id="bea34-108">如需 Windows Vista 中系統效果的詳細資訊，請參閱 Windows 網站的 [音訊裝置技術](https://www.microsoft.com/whdc/device/audio/default.mspx) 上標題為「windows Vista 的自訂音訊效果」和「重複使用 Windows Vista 音訊系統效果」的白皮書。</span><span class="sxs-lookup"><span data-stu-id="bea34-108">For more information about system effects in Windows Vista, see the white papers titled "Custom Audio Effects in Windows Vista" and "Reusing Windows Vista Audio System Effects" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="bea34-109">這個屬性只適用于安裝了端點裝置所連接之音訊介面卡的 .inf 檔案所安裝的本機效果和全域效果。</span><span class="sxs-lookup"><span data-stu-id="bea34-109">This property applies only to the local-effects and global-effects APOs that were installed by the .inf file that installed the audio adapter to which the endpoint device is connected.</span></span> <span data-ttu-id="bea34-110">此外，此屬性只會影響目標端點裝置，即使是連接到相同的介面卡，也不會影響任何其他端點裝置的系統效果。</span><span class="sxs-lookup"><span data-stu-id="bea34-110">In addition, this property affects only the target endpoint device—it has no effect on the system effects for any other endpoint devices, even if they connect to the same adapter.</span></span>

<span data-ttu-id="bea34-111">**PROPVARIANT** 結構的 **vt** 成員會設定為 **vt \_ UI4**。</span><span class="sxs-lookup"><span data-stu-id="bea34-111">The **vt** member of the **PROPVARIANT** structure is set to **VT\_UI4**.</span></span>

<span data-ttu-id="bea34-112">如果啟用了系統效果，或如果已停用 **端點 \_ \_ SYSFX** ，則 **PROPVARIANT** 結構的 **ulVal** 成員會設定為 **\_ \_ 已啟用的 endpoint SYSFX** 。</span><span class="sxs-lookup"><span data-stu-id="bea34-112">The **ulVal** member of the **PROPVARIANT** structure is set to **ENDPOINT\_SYSFX\_ENABLED** if system effects are enabled or to **ENDPOINT\_SYSFX\_DISABLED** if they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea34-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bea34-113">Requirements</span></span>



| <span data-ttu-id="bea34-114">需求</span><span class="sxs-lookup"><span data-stu-id="bea34-114">Requirement</span></span> | <span data-ttu-id="bea34-115">值</span><span class="sxs-lookup"><span data-stu-id="bea34-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bea34-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bea34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bea34-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bea34-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bea34-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bea34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bea34-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bea34-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bea34-120">標頭</span><span class="sxs-lookup"><span data-stu-id="bea34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bea34-121"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="bea34-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea34-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bea34-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea34-123">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="bea34-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="bea34-124">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="bea34-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




