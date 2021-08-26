---
title: 動作和許可權
description: 動作和許可權
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- 'Windows媒體格式 SDK、數位版權管理 (DRM) '
- Windows媒體格式 SDK，DRM 授權
- Windows媒體格式 SDK，DRM 的授權
- 數位版權管理 (DRM) ，動作
- DRM (數位版權管理) ，動作
- 數位版權管理 (DRM) ，權利
- DRM (數位版權管理) ，權利
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 授權，DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b822c0350af12c5e266570a031ca0d3eda7c99b4b8451b751786a60a4a0908d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089768"
---
# <a name="actions-and-rights"></a>動作和許可權

使用 Windows 媒體 DRM 保護檔案時，會完全限制其使用方式。 您可以發出授權，讓使用者以特定方式使用內容。 使用者可能使用內容的每種方式都是由動作描述。 例如，在電腦上播放檔案是一個動作。

啟用指定動作的授權稱為授與許可權。 例如，授權可以授與在電腦上播放內容的許可權。

動作和許可權指的是使用內容的相同方式。 不同之處在于動作會參考使用，而許可權則是指許可權。 儘管有此差異，在本檔和描述 Windows 媒體 DRM 的其他檔中，通常會交替使用「動作」和「許可權」等字。

受 Windows 媒體 DRM 許可權控管的動作會列在本檔的[許可權常數](rights-constants.md)一節中。

Windows 媒體 DRM 用戶端擴充 api 的某些方法會使用不同的常數來參考基本的 DRM 許可權。 例如， [**IWMDRMLicenseQuery：： QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) 方法會使用一組特定于授權狀態的字串。 雖然這些常數是定義與基本許可權常數不同的字串，但它們會參考授權中的相同許可權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**概念**](drmconcepts.md)
</dt> </dl>

 

 




