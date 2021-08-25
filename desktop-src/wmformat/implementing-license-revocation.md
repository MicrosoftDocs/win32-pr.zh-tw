---
title: 執行授權撤銷
description: 執行授權撤銷
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows媒體格式 SDK，執行授權撤銷
- Windows媒體格式 SDK，授權撤銷
- Windows媒體格式 SDK，撤銷授權
- Advanced Systems Format (ASF) ，實施授權撤銷
- ASF (Advanced Systems Format) ，實施授權撤銷
- Advanced Systems Format (ASF) 、授權撤銷
- ASF (Advanced 系統格式) 、授權撤銷
- Advanced Systems Format (ASF) ，撤銷授權
- ASF (Advanced Systems Format) ，撤銷授權
- 數位版權管理 (DRM) ，實施授權撤銷
- DRM (數位版權管理) ，實施授權撤銷
- 數位版權管理 (DRM) 、授權撤銷
- DRM (數位版權管理) 、授權撤銷
- 數位版權管理 (DRM) ，撤銷授權
- DRM (數位版權管理) ，撤銷授權
- 授權撤銷，實施
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c73d0204e83c941600eefb53579b19ef72217055080c6ef4603d8eac28e08caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809128"
---
# <a name="implementing-license-revocation"></a>執行授權撤銷

Windows 媒體版權管理員 10 SDK 包含稱為「許可證撤銷」的功能。 這項功能可讓授權伺服器要求從用戶端電腦移除授權。 Windows 媒體格式 SDK 提供的方法可處理撤銷訊息，以及從本機授權存放區移除授權。

授權撤銷程式是由授權簽發者所提供的服務所起始。 您的應用程式可以裝載此服務，也可以是 Web 應用程式。 無論是哪一種情況，您的應用程式都必須能夠收到服務所建立的授權挑戰。

若要移除授權存放區的授權，請執行下列步驟：

1.  收到授權簽發者的授權挑戰時，請呼叫 [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) 函式來建立授權撤銷代理程式物件，並取得 [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) 介面的指標。
2.  呼叫 [**IWMLicenseRevocationAgent：： GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) 方法，以產生挑戰回應。
3.  將挑戰回應傳送回您收到挑戰的授權服務元件。
4.  授權服務元件會將已簽署的授權撤銷 blob (LRB) 傳送至您的應用程式。 當您收到時，請呼叫 [**IWMLicenseRevocationAgent：:P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) 方法。 **ProcessLRB** 會建立通知訊息，您必須將其傳回給授權服務，以確認已移除授權。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**IWMLicenseRevocationAgent 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




