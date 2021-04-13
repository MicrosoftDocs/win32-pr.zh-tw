---
title: 連接到 Windows Media Player
description: 連接到 Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Windows Media Player 外掛程式、登錄專案
- 外掛程式，登錄專案
- Windows Media Player 外掛程式，連接
- 外掛程式，連接
- 數位信號處理外掛程式，連接
- DSP 外掛程式，連接
- 數位信號處理外掛程式，登錄專案
- DSP 外掛程式，登錄專案
- 登錄、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374379"
---
# <a name="connecting-to-windows-media-player"></a><span data-ttu-id="62bfd-112">連接到 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="62bfd-112">Connecting to Windows Media Player</span></span>

<span data-ttu-id="62bfd-113">Windows Media Player 會自動連接到已安裝並正確註冊的 DSP 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="62bfd-113">Windows Media Player automatically connects to DSP plug-ins that have been installed and properly registered.</span></span> <span data-ttu-id="62bfd-114">DSP 外掛程式必須呼叫 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 來建立必要的登錄專案，以允許 Windows Media Player 辨識外掛程式，並將其列在 [選項] 對話方塊的 [ **外掛程式** ] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="62bfd-114">DSP plug-ins must call [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) to create the registry entries necessary to allow Windows Media Player to recognize the plug-in and to list it on the **Plug-ins** tab of the Options dialog box.</span></span> <span data-ttu-id="62bfd-115">若要移除 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** 建立的登錄專案，外掛程式會呼叫 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin)。</span><span class="sxs-lookup"><span data-stu-id="62bfd-115">To remove the registry entries created by **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, the plug-in calls [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62bfd-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="62bfd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62bfd-117">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="62bfd-117">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




