---
title: 建立主要動畫物件
description: 若要在您的應用程式中使用 Windows 動畫，第一個步驟就是建立一組小型的主要動畫物件。
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- 動畫管理員物件視窗動畫，建立
- 動畫計時器物件視窗動畫，建立
- 轉換程式庫物件視窗動畫，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376256"
---
# <a name="create-the-main-animation-objects"></a>建立主要動畫物件

若要在您的應用程式中使用 Windows 動畫，第一個步驟就是建立一組小型的主要動畫物件。

## <a name="overview"></a>概觀

使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數可建立動畫管理員、動畫計時器和轉換程式庫物件。

建立和顯示動畫時需要這些物件，因此在應用程式關閉之前，通常不應該釋出這些物件。 如果任何已註冊的回呼都沒有機會建立參考迴圈，釋出物件就足以進行適當的清除。 否則，應用程式可以清除回呼， (在每個) 的位置傳遞 **Null** ，或藉由呼叫動畫管理員的 [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) 方法來進行清除。

## <a name="example-code"></a>範例程式碼

下列範例程式碼取自 Windows 動畫範例中的 MainWindow：請參閱 CMainWindow：： InitializeAnimation 方法。


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



請注意 MainWindow 的下列定義。


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a>後續步驟

完成此步驟後，下一個步驟是： [建立動畫變數](create-animation-variables.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationTimer**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[Windows 動畫總覽](scenic-animation-api-overview.md)
</dt> </dl>

 

 