---
title: 讀取受保護的檔案
description: 讀取受保護的檔案
ms.assetid: 24f839f1-ce57-4d06-b1a5-a6bea7b5b7bb
keywords:
- Windows Media Format SDK，讀取受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，讀取受保護的檔案
- ASF (Advanced 系統格式) ，讀取受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，讀取受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b2110708a28daae1e86ba3dac2ea1f18ad16fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681386"
---
# <a name="reading-protected-files"></a>讀取受保護的檔案

讀取受 DRM 保護的檔案或網路資料流程基本上牽涉到嘗試開啟檔案 (或連接到資料流程) 然後處理任何可能從 DRM 元件傳送的事件。

如果播放程式不是啟用 DRM 的 (不會連結至有效的 wmstubdrm .lib 程式庫) [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 呼叫會在嘗試開啟受保護的檔案時失敗，並傳回 NS \_ E \_ 受保護的 \_ 內容或某些相關錯誤。

當啟用 DRM 的應用程式嘗試開啟受 DRM 保護的檔案時，DRM 元件會自動搜尋本機系統是否有有效的授權。 如果找到一個，DRM 元件會自動以對應用程式完全透明的方式來解密檔案。 應用程式可在解密檔案上執行的動作取決於授權中指定的許可權。 如需可能許可權的完整說明，請參閱 Windows Media Rights Manager SDK 檔。

如果應用程式沒有有效的檔案授權，播放程式會收到來自 DRM 元件的狀態通知。 然後，播放程式應用程式可以起始 [*授權*](wmformat-glossary.md) 取得程式。 收到有效的授權之後，就可以存取該檔案。 下列各節描述應用程式在執行授權取得程式時必須執行的基本工作：

-   [指定要執行的動作](specifying-the-actions-to-be-performed.md)
-   [處理授權取得事件](handling-license-acquisition-events.md)
-   [Individualizing DRM 應用程式](individualizing-drm-applications.md)
-   [處理個人化事件](handling-individualization-events.md)

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 




