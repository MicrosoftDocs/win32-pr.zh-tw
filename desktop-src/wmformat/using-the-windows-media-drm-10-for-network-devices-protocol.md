---
title: 使用 Windows Media DRM 10 進行網路裝置通訊協定
description: 使用 Windows Media DRM 10 進行網路裝置通訊協定
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media Format SDK，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Windows Media Format SDK、DRM 10
- Advanced Systems Format (ASF) 、適用于網路裝置的 Windows Media DRM 10
- ASF (Advanced Systems Format) ，適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的 Advanced Systems Format (ASF) ，DRM 10
- ASF (Advanced Systems Format) ，DRM 10 用於網路裝置
- 數位版權管理 (DRM) ，適用于網路裝置的 Windows Media DRM 10
- DRM (數位版權管理) 、適用于網路裝置的 Windows Media DRM 10
- 適用于網路裝置的數位版權管理 (DRM) ，DRM 10
- DRM (數位版權管理) ，DRM 10 用於網路裝置
- 適用于網路裝置的 Windows Media DRM 10，通訊協定
- 適用于網路裝置、通訊協定的 DRM 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300724"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>使用 Windows Media DRM 10 進行網路裝置通訊協定

Windows Media Format SDK 提供一些功能，可支援網路裝置的安全網路裝置通訊協定，也就是 Windows Media DRM 10。 此通訊協定會定義數位媒體播放裝置間傳送的訊息，例如機頂尖的影片播放程式，以及提供資料給裝置的電腦。 在伺服器與裝置之間傳送的媒體資料會經過加密，以防止其遭到攔截。

您的應用程式與支援網路裝置 Windows Media DRM 10 的裝置之間的通訊，可以使用您偏好的任何網路通訊協定。 Windows Media Format SDK 不提供任何為您執行網路通訊的物件。 相反地，此 SDK 的物件會在您的應用程式收到訊息之後，為網路裝置的訊息處理一些 Windows Media DRM 10。

針對網路裝置支援 Windows Media DRM 10 的功能包括裝置註冊、鄰近性偵測，以及轉換受 DRM 保護的檔案。 這些功能將在下列各節中說明。



| 區段                                                                                                                                                                          | 描述                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [裝置註冊](device-registration.md)                                                                                                                                   | 說明如何處理來自裝置的註冊要求訊息。                                                                       |
| [執行鄰近性偵測](performing-proximity-detection.md)                                                                                                             | 描述鄰近性偵測處理常式。                                                                                                 |
| [將 DRM-Protected 檔案轉換為網路裝置串流的 Windows Media DRM 10](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | 描述如何將受 DRM 保護的檔案轉換成可以傳送至裝置的串流，該裝置會針對網路裝置使用 Windows Media DRM 10。 |



 

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




