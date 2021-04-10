---
title: 程式庫檔案、標頭檔和編譯器設定
description: 程式庫檔案、標頭檔和編譯器設定
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media Format SDK，DRM 程式庫檔案
- Windows Media Format SDK，程式庫檔案
- Windows Media Format SDK，DRM 標頭檔
- Windows Media Format SDK，標頭檔
- Windows Media Format SDK，DRM 編譯器設定
- Windows Media Format SDK，編譯器設定
- 數位版權管理 (DRM) 、程式庫檔案
- DRM (數位版權管理) 、程式庫檔案
- 數位版權管理 (DRM) ，標頭檔
- DRM (數位版權管理) ，標頭檔
- 數位版權管理 (DRM) ，編譯器設定
- DRM (數位版權管理) ，編譯器設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092282"
---
# <a name="library-files-header-files-and-compiler-settings"></a>程式庫檔案、標頭檔和編譯器設定

Windows Media DRM 用戶端擴充 Api 的程式設計元件定義于 wmdrmsdk .h 標頭檔中，並在 wmdrmsdk .lib 和 mfuuid .lib 程式庫中執行。

Windows Media DRM 用戶端擴充 Api 的部分功能需要您從 Microsoft 取得受保護的程式庫。 本檔中稱為存根程式庫的程式庫是由收件者所特有，並指定應用程式的應用程式安全性層級。 存根程式庫會取代 wmdrmsdk。您永遠都不應該連結到兩者。

**注意** DRM 存根程式庫與 Windows Media Format SDK 其餘部分所使用的存根程式庫不同，但會使用相同的方法來授權。

**注意** 在程式庫檔案 msvcrt.lib 之後，必須將 DRM 存根程式庫連結至您的應用程式，以避免連結器錯誤。

如果您無法遵守授權合約的條款與條件，則存根程式庫包含可由 Microsoft 撤銷的內嵌憑證。

檔中會標示需要存根程式庫的特定方法。 如果您嘗試使用這類方法而不連結到存根程式庫，則會傳回 NS \_ E \_ DRM \_ STUBLIB \_ 必要錯誤。

DRM 子系統不能用在 debug 組建中。 如果嘗試這麼做，API 的方法將會傳回 NS \_ E \_ DRM 不允許的偵測 \_ \_ \_ 錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](drm-getting-started.md)
</dt> <dt>

[**程式庫檔案和編譯器設定**](library-files-and-compiler-settings.md)
</dt> <dt>

[**取得必要的 DRM 程式庫**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




