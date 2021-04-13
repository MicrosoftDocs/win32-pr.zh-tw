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
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="06776-106">建立主要動畫物件</span><span class="sxs-lookup"><span data-stu-id="06776-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="06776-107">若要在您的應用程式中使用 Windows 動畫，第一個步驟就是建立一組小型的主要動畫物件。</span><span class="sxs-lookup"><span data-stu-id="06776-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="06776-108">概觀</span><span class="sxs-lookup"><span data-stu-id="06776-108">Overview</span></span>

<span data-ttu-id="06776-109">使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數可建立動畫管理員、動畫計時器和轉換程式庫物件。</span><span class="sxs-lookup"><span data-stu-id="06776-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="06776-110">建立和顯示動畫時需要這些物件，因此在應用程式關閉之前，通常不應該釋出這些物件。</span><span class="sxs-lookup"><span data-stu-id="06776-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="06776-111">如果任何已註冊的回呼都沒有機會建立參考迴圈，釋出物件就足以進行適當的清除。</span><span class="sxs-lookup"><span data-stu-id="06776-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="06776-112">否則，應用程式可以清除回呼， (在每個) 的位置傳遞 **Null** ，或藉由呼叫動畫管理員的 [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) 方法來進行清除。</span><span class="sxs-lookup"><span data-stu-id="06776-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="06776-113">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="06776-113">Example Code</span></span>

<span data-ttu-id="06776-114">下列範例程式碼取自 Windows 動畫範例中的 MainWindow：請參閱 CMainWindow：： InitializeAnimation 方法。</span><span class="sxs-lookup"><span data-stu-id="06776-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


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



<span data-ttu-id="06776-115">請注意 MainWindow 的下列定義。</span><span class="sxs-lookup"><span data-stu-id="06776-115">Note the following definitions from MainWindow.h.</span></span>


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



## <a name="next-step"></a><span data-ttu-id="06776-116">後續步驟</span><span class="sxs-lookup"><span data-stu-id="06776-116">Next Step</span></span>

<span data-ttu-id="06776-117">完成此步驟後，下一個步驟是： [建立動畫變數](create-animation-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="06776-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06776-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="06776-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06776-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="06776-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="06776-120">**IUIAnimationManager**</span><span class="sxs-lookup"><span data-stu-id="06776-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="06776-121">**IUIAnimationTimer**</span><span class="sxs-lookup"><span data-stu-id="06776-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="06776-122">**IUIAnimationTransitionLibrary**</span><span class="sxs-lookup"><span data-stu-id="06776-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="06776-123">Windows 動畫總覽</span><span class="sxs-lookup"><span data-stu-id="06776-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 