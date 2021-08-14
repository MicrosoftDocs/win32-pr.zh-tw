---
title: 使用 Microsoft Windows 媒體 DRM 用戶端程式代碼範例
description: 使用 Microsoft Windows 媒體 DRM 用戶端程式代碼範例
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows媒體格式 SDK，程式碼範例
- Windows媒體格式 SDK，範例程式碼
- Windows媒體格式 SDK，DRM 程式碼範例
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704211"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>使用 Microsoft Windows 媒體 DRM 用戶端程式代碼範例

本檔中包含程式碼範例，以說明元件的使用方式。 這些範例會盡可能清楚且簡潔地撰寫。 閱讀範例時，您應該注意下列慣例。

-   所有範例都假設為包含 windows .h 和 wmdrmsdk .h。 如果需要其他標頭才能進行編譯，此範例將包含附注。
-   如果發生錯誤，則錯誤檢查已限制為無法中斷函數。 在應用程式中，您應該檢查特定的錯誤碼，並提供某種類型的錯誤報表。
-   在程式碼範例中，會使用名為 SAFE \_ RELEASE 和 safe \_ ARRAY DELETE 的宏來釋放介面和記憶體 \_ 。 這些宏會在下列程式碼中定義：
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**開始使用**](drm-getting-started.md)
</dt> </dl>

 

 




