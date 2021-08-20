---
title: 建立分鏡腳本並新增轉換
description: 若要建立動畫，應用程式必須建立分鏡腳本。
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- 分鏡腳本 Windows 動畫，建立
- 分鏡腳本 Windows 動畫、新增轉換
- Windows 動畫的轉換，建立
- Windows 動畫的轉換，加入至分鏡腳本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999638"
---
# <a name="create-a-storyboard-and-add-transitions"></a>建立分鏡腳本並新增轉換

若要建立動畫，應用程式必須建立分鏡腳本。

## <a name="overview"></a>概觀

建立分鏡腳本的一般步驟如下：

1.  建立分鏡腳本
2.  建立一或多個轉換
3.  將轉換新增至腳本，並指定其製作動畫的變數

您可以使用動畫管理員來建立空白的分鏡腳本。 應用程式必須在每個分鏡腳本中填入轉換。 每個轉換會指定單一動畫變數在指定時間間隔內的變更方式。 您可以使用 Windows 動畫中包含的轉換程式庫元件來建立轉換。 或者，應用程式可以建立自己的自訂轉換，或使用協力廠商的轉換程式庫。 當應用程式將轉換新增至分鏡腳本時，它會指定轉換將會製作動畫的動畫變數。

分鏡腳本可包含一或多個動畫變數上的轉換。 更複雜的分鏡腳本可以使用主要畫面格來同步處理轉換的開始或結束，或是指定應重複 (固定次數或無限) 的分鏡腳本部分。

## <a name="example-code"></a>範例程式碼

下列範例程式碼取自 Windows 動畫範例[計時器驅動動畫](timer-driven-animation-sample.md)中的 MainWindow。請參閱 CMainWindow：： ChangeColor 方法。 此範例會使用 [**IUIAnimationManager：： CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) 方法建立分鏡腳本 (步驟 1) 、使用 [**IUIAnimationTransitionLibrary：： CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) 方法建立轉換 (步驟 2) ，然後使用 [**IUIAnimationStoryboard：： AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) 方法將轉換新增至分鏡腳本 (步驟 3) 。


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a>上一個步驟

開始此步驟之前，您應該已完成此步驟： [讀取動畫變數值](updating---application-driven-animation.md)。

## <a name="next-step"></a>後續步驟

完成此步驟後，下一個步驟是： [排程分](scheduling-a-storyboard.md)鏡腳本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[分鏡腳本總覽](storyboard-construction.md)
</dt> </dl>

 

 




