---
description: PKEY \_ AudioEndpoint \_ ControlPanelPageProvider 屬性會指定音訊端點裝置之裝置屬性延伸模組的已註冊提供者 CLSID。
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: 'PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847308"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a><span data-ttu-id="61b1d-103">PKEY \_ AudioEndpoint \_ ControlPanelPageProvider</span><span class="sxs-lookup"><span data-stu-id="61b1d-103">PKEY\_AudioEndpoint\_ControlPanelPageProvider</span></span>

<span data-ttu-id="61b1d-104">**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider** 屬性會指定音訊端點裝置之裝置屬性延伸模組的已註冊提供者 CLSID。</span><span class="sxs-lookup"><span data-stu-id="61b1d-104">The **PKEY\_AudioEndpoint\_ControlPanelPageProvider** property specifies the CLSID of the registered provider of the device-properties extension for the audio endpoint device.</span></span> <span data-ttu-id="61b1d-105">此延伸模組會提供在 [Windows 多媒體] 控制台的 [裝置內容] 頁面中顯示的音訊端點屬性，Mmsys.cpl。</span><span class="sxs-lookup"><span data-stu-id="61b1d-105">The extension supplies the audio endpoint properties that are displayed in the device-properties page of the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="61b1d-106">如需 Mmsys.cpl 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="61b1d-106">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="61b1d-107">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ LPWSTR。</span><span class="sxs-lookup"><span data-stu-id="61b1d-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="61b1d-108">**PROPVARIANT** 結構的 **pwszVal** 成員指向以 null 結尾的寬字元字串，其中包含可識別控制台擴充功能提供者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="61b1d-108">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the provider of the control-panel extension.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b1d-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="61b1d-109">Requirements</span></span>



| <span data-ttu-id="61b1d-110">需求</span><span class="sxs-lookup"><span data-stu-id="61b1d-110">Requirement</span></span> | <span data-ttu-id="61b1d-111">值</span><span class="sxs-lookup"><span data-stu-id="61b1d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b1d-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61b1d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="61b1d-113">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61b1d-113">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="61b1d-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61b1d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="61b1d-115">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61b1d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="61b1d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="61b1d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="61b1d-117"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="61b1d-117"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b1d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61b1d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b1d-119">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="61b1d-119">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="61b1d-120">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="61b1d-120">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




