---
title: 處理個人化事件
description: 處理個人化事件
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows媒體格式 SDK，處理個人化設定事件
- Windows媒體格式 SDK、個人化事件
- Advanced Systems Format (ASF) ，處理個人化事件
- ASF (Advanced Systems Format) ，處理個人化事件
- Advanced Systems Format (ASF) 、個人化事件
- ASF (Advanced Systems Format) 、個人化事件
- 數位版權管理 (DRM) ，處理個人化事件
- DRM (數位版權管理) ，處理個人化事件
- 數位版權管理 (DRM) 、個人化事件
- DRM (數位版權管理) 、個人化事件
- 個人化事件
- 事件、個人化事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895710558c58fca108915ad1a73a0354c1fb39feb662fa3e2c698dadbe4cbe76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433612"
---
# <a name="handling-individualization-events"></a>處理個人化事件

當啟用 DRM 的應用程式嘗試開啟受保護的檔案時，DRM 元件會檢查檔案中的 [**drm \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) 屬性，此屬性會指定存取內容所需的最低版本層級。 DRM 元件的所有層級都適用于所有7.0 和更新版本的 Windows Media Player 和 Windows 媒體格式 SDK。 如果 DRM 元件的個別版本層級低於所需的版本，DRM 元件會將 **WMT \_ 需要 \_** 的「個人化」事件傳送至應用程式的 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法。 然後，應用程式必須顯示訊息或對話方塊，提示使用者啟動或取消安全性升級。 這是必要的提示，因為基於隱私權考慮，使用者必須在其電腦上安裝安全性升級之前授與其許可權。

> [!Note]  
> 內容的標頭只會指定 DRM DRMVersion IndividualizedVersion 的前兩個數字 \_ \_ 。 換句話說，若要要求層級 2.2.0.1 DRM 元件，標頭會包含 "2.2"。

 

若要啟動安全性升級及/或觸發程式的個人化設定，請呼叫 [**IWMDRMReader：：賦予**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) 方法，並將 *dwFlags* 參數設定為1。

您必須在應用程式中處理 **WMT \_ 賦予** 事件。 DRM 元件會引發此事件多次，其具有在 *pValue* 參數中指定的個人化程式狀態，這會轉換為 [**WM \_ 賦予 \_ 狀態**](wm-individualize-status.md) 結構的指標。

在 DRM 元件成功個人化之後，應用程式將會收到 **WMT \_ 無 \_ 許可權的 \_ EX** 事件，指出應用程式現在可以繼續取得內容的授權。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**處理授權取得事件**](handling-license-acquisition-events.md)
</dt> <dt>

[**Individualizing DRM 應用程式**](individualizing-drm-applications.md)
</dt> <dt>

[**IWMDRMReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




