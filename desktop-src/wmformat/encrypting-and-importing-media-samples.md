---
title: 加密和匯入媒體範例
description: 加密和匯入媒體範例
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows媒體格式 SDK，DRM 匯入
- Windows媒體格式 SDK，匯入
- Windows媒體格式 SDK，加密媒體範例
- 數位版權管理 (DRM) ，匯入
- DRM (數位版權管理) ，匯入
- 數位版權管理 (DRM) ，加密媒體範例
- DRM (數位版權管理) ，加密媒體範例
- DRM 用戶端擴充 Api，匯入
- 用戶端擴充 Api，匯入
- DRM 用戶端擴充 Api，加密媒體範例
- 用戶端擴充 Api，加密媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed604fc114feed6bd308b9a89c6bde6d6c96abeb9e88a7b9ace19d553de1596
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658838"
---
# <a name="encrypting-and-importing-media-samples"></a>加密和匯入媒體範例

針對使用 Windows 媒體 DRM 進行加密的每個媒體範例，您必須產生嚴格大於上一個的 salt 值 (單純增加) 。 使用新的 salt 值建立暫時性加密金鑰，方法是將 SHA-1 加密演算法套用至與 salt 值串連的初始化向量。

接下來，使用所產生的暫時性金鑰，根據 RC4 演算法來加密範例。 將範例傳遞給 SDK 之前，您的應用程式必須藉由設定擴充屬性來建立 salt 值與範例之間的關聯。

以下是加密媒體範例的步驟：

1.  呼叫範例物件的 **QueryInterface** 方法，以取得 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) 介面。
2.  遞增 salt 值。
3.  使用 RC1 加密演算法來加密範例。 針對加密，您會串連初始化向量和 salt 值來建立金鑰。
4.  藉由呼叫 [**INSSBuffer：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty)將 salt 值提供給 SDK。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DRM 匯入**](drm-import.md)
</dt> <dt>

[**媒體範例加密範例**](media-sample-encryption-example.md)
</dt> </dl>

 

 




