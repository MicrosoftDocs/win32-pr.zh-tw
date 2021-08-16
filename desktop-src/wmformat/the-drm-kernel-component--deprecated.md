---
title: 'DRM 核心元件 (已淘汰) '
description: 'DRM 核心元件 (已淘汰) '
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- 'Windows媒體格式 SDK、Microsoft 安全音訊路徑 (SAP) '
- '數位版權管理 (DRM) 、Microsoft 安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 、Microsoft 安全音訊路徑 (SAP) '
- Windows媒體格式 SDK， (SAP) 的安全音訊路徑
- '數位版權管理 (DRM) 的安全音訊路徑 (SAP) '
- 'DRM (數位版權管理) 的安全音訊路徑 (SAP) '
- Windows媒體格式 SDK，DRM 核心元件
- 數位版權管理 (DRM) ，核心元件
- DRM (數位版權管理) ，核心元件
- " (SAP) ，DRM 核心元件的 Microsoft 安全音訊路徑"
- " (SAP) ，DRM 核心元件的安全音訊路徑"
- SAP (安全音訊路徑) ，DRM 核心元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8db4389d9156ef13d9e87983a4ae433e6028805268f3cbd55690d4d0d8144b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845755"
---
# <a name="the-drm-kernel-component-deprecated"></a>DRM 核心元件 (已淘汰) 

本頁面記載了在未來版本的 Windows 中，將會受到不同技術解決方案支援的功能。

在 Microsoft 安全音訊路徑 (SAP) 模型中，DRM 核心元件提供兩項基本功能，可保護加密音樂的完整性。

首先，當播放音樂檔案時，DRM 用戶端元件和 DRM 核心元件會進行通訊。 這兩個元件之間的通訊，可防止任何人篡改加密信號或插入 false 資訊。

其次，在所有剩餘的元件都經過驗證之前，DRM 核心元件不會將音樂信號解密。 也就是說，在解密內容並將它傳遞給下一個系統元件之前，DRM 核心元件會檢查每個可存取內容) 的元件 (每個元件的路徑，並確認這些元件已使用 Microsoft 的憑證進行簽署。 未簽署的元件可能表示有可疑的元件或惡意的驅動程式。 因此，當 DRM 核心元件驗證剩餘的元件時，如果有任何元件無法進行這項測試，則信號會暫停且無法播放。 否則，如果所有元件都通過驗證，DRM 核心元件會將音樂解密，並將其傳遞給下一個元件。

Microsoft 數位簽署的驅動程式，可傳遞 Windows®硬體品質實驗室 (WHQL) 測試，以確保使用者使用最高品質的驅動程式。 這是標準的做法，可確保元件的真實性，因為簽章無法偽造，也不能修改程式碼，而不會終結簽章。 經認證的安全音訊路徑的驅動程式，必須保護其所處理的音訊資料免于受信任元件的存取。 

Windows Millennium Edition 和 Windows XP 隨附的驅動程式會更新為安全音訊路徑並簽署。 未簽署可搭配 Windows 我或 Windows XP 使用的驅動程式無法播放受保護的音樂。 驅動程式製造商可以重新發出經 WHQL 簽署的更新版驅動程式，並將其發佈到網際網路供取用者下載。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Microsoft 安全音訊路徑**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




