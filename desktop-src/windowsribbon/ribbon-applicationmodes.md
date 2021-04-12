---
title: 使用應用程式模式重新設定功能區
description: Windows 功能區架構支援在執行時間以動態方式重新設定和公開功能區 UI 的核心元素，並根據應用程式的狀態 (也稱為內容) 。
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Windows 功能區，以應用程式模式重新設定
- 功能區，以應用程式模式重新設定
- 使用應用程式模式重新設定 Windows 功能區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375349"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>使用應用程式模式重新設定功能區

Windows 功能區架構支援在執行時間以動態方式重新設定和公開功能區 UI 的核心元素，並根據應用程式的狀態 (也稱為內容) 。 宣告並與標記中的特定元素相關聯時，應用程式支援的各種狀態稱為應用程式模式。

-   [簡介](#introduction)
-   [內容相關消費者介面](#contextual-user-interface)
    -   [簡單的應用程式模式案例](#a-simple-application-mode-scenario)
-   [執行應用程式模式](#implementing-application-modes)
    -   [識別模式](#identify-the-modes)
    -   [將控制項指派給應用程式模式](#assign-controls-to-application-modes)
    -   [執行時間切換模式](#switch-modes-at-runtime)
-   [備註](#remarks)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

應用程式模式是由控制項的邏輯群組所組成，這些控制項會公開功能區 UI 中的一些核心應用程式功能。 這些模式是由應用程式透過呼叫 framework 方法 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)來動態啟用或停用，它會開啟或關閉一或多個應用程式模式的可見度。

## <a name="contextual-user-interface"></a>內容相關消費者介面

功能區架構藉由併入可順暢地回應使用者互動和應用程式內容的動態控制項，來提供豐富的使用者體驗。 此豐富的內容 UI 是透過下列機制的組合提供：

-   資源庫-以集合為基礎的控制項，支援其專案集合的動態操作。
-   內容索引標籤-功能區索引標籤，其可見度是由工作區內容的變更所決定，例如檔中的影像選取範圍。
-   應用程式模式-相依于應用程式內容的核心應用程式功能。

在某些方面，應用程式模式的功能類似于內容索引標籤。 不過，基本的差異在於各自的意圖和範圍中。

啟用內容控制項以回應應用程式內的內容變更。 例如，在 Windows 7 的 Microsoft 小畫家中，當使用者將文字區域插入工作區時，會顯示包含文字相關命令群組的內容索引標籤。 此內容索引標籤不包含應用程式的核心命令，而且只會在 UI 中公開，因為應用程式 *中* 的內容已變更。 應用程式的核心功能 (影像編輯命令) 仍相關且可供使用者使用，即使是可見的內容索引標籤。

應用程式模式與內容相關的控制項不同之處在于，它們會重新設定功能，以回應應用程式運作的內容變更。 應用程式模式位於較高層級的抽象層級;它們提供一種方式來重新設定應用程式的核心功能，而不是暫時公開不是 UI 核心元件的功能。 例如，在 Windows 7 的 Microsoft 小畫家中，當叫用 **預覽列印** 命令時，會在應用程式模式中切換。 當 Microsoft 小畫家切換至 [ **預覽列印**] 時，應用程式正在操作的內容會從編輯變更為預覽。 如此一來，應用程式的核心功能就會變更，直到取消 **預覽列印** ，且應用程式再次進入編輯內容為止。

### <a name="a-simple-application-mode-scenario"></a>簡單的應用程式模式案例

下列案例示範如何在名為 RibbonApp 的應用程式中使用應用程式模式，以公開核心功能的不同部分。

RibbonApp 中定義了兩個應用程式模式：

-   **簡單** 模式會公開整個功能區 UI 中的基本命令。 無論使用哪一種應用程式模式，這些命令都會出現在任何時候。
-   **Advanced** 模式會公開適用于應用程式專家使用者的複雜命令。 除了簡單的命令之外，這些 advanced 命令也會出現在功能區 UI 中。

依預設，RibbonApp 會設定為 [在 **簡單** 模式中開啟]，而且會在 [ **應用程式] 功能表** 和 [ **主** 資料夾] 索引標籤中顯示使用者所需的命令。下列螢幕擷取畫面顯示簡單模式下的 [RibbonApp **應用程式] 功能表** 和 [ **首頁** ] 索引 **卷** 標，並醒目提示模式控制項。

![顯示簡單應用程式模式索引標籤的螢幕擷取畫面。](images/overviews/appmode-hometab.png)![顯示簡單應用程式模式應用程式功能表的螢幕擷取畫面。](images/overviews/appmode-simpleappmenu.png)

雖然這些命令對新手使用者而言可能已足夠，但 RibbonApp 也會透過 **Advanced** 模式支援專家使用者，當您按一下 **應用程式功能表** 中的 [**切換到 Advanced mode]** 按鈕來啟動時，就會顯示其他的核心功能。

藉由將標記中的各種元素系結至可依需要開啟和關閉的離散應用程式模式，即可輕鬆地執行此案例。 下列螢幕擷取畫面顯示 [ **Advanced** ] 模式中的 [RibbonApp **應用程式] 功能表** 和 [**首頁**] 索引標籤，並醒目提示模式控制項。

![顯示 [advanced] 應用程式模式索引標籤的螢幕擷取畫面。](images/overviews/appmode-advancedtab.png)![顯示 [advanced application] 模式的 [應用程式] 功能表的螢幕擷取畫面。](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>執行應用程式模式

本節將概述功能區架構應用程式模式的執行通常需要的三個步驟。 RibbonApp 是用來提供每個步驟的範例。

### <a name="identify-the-modes"></a>識別模式

應用程式中的每個模式都應該代表一組邏輯功能，這取決於應用程式能夠操作的內容。 例如，如果應用程式顯示的控制項只有在偵測到網路連接時才有關聯，這些控制項就會在網路內容中運作，而這可能會讓 **網路** 模式的建立。

RibbonApp 有兩個在任何指定時間都可以處於作用中的內容： **Simple** 和 **Advanced**。 因此，RibbonApp 需要兩種模式： **Simple** 和 **Advanced**。

### <a name="assign-controls-to-application-modes"></a>將控制項指派給應用程式模式

一旦識別出應用程式模式之後，請在支援應用程式模式的控制項元素的標記中宣告 *ApplicationModes* 屬性，將每個功能區控制項指派給模式。

功能區視圖可讓您在下列控制項元素上指定模式：

-   核心 [**選項卡**](windowsribbon-element-tab.md) 元素。
-   [**群組**](windowsribbon-element-group.md) 專案 [**是核心索引**](windowsribbon-element-tab.md) 標籤元素的子項目。
-   指派給 [應用程式功能表](windowsribbon-controls-applicationmenu.md)內 [**MenuGroup**](windowsribbon-element-menugroup.md)的 [**按鈕**](windowsribbon-element-button.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)和 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)元素。
    > [!Note]  
    > 除非裝載于 [[應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中，否則無法將 [**Button**](windowsribbon-element-button.md)、 [**SplitButton**](windowsribbon-element-splitbutton.md)和 [**DropDownButton**](windowsribbon-element-dropdownbutton.md)元素指派給模式。

     

在功能區架構中，這些控制項元素稱為強制回應控制項。 只有當其系結的模式在 UI 中為作用中時，才會顯示它們。

包含在強制回應控制項內的控制項元素，會繼承應用程式模式的行為。 例如，如果將 [**群組**](windowsribbon-element-group.md) 強制回應控制項指派給 **advanced** 模式，而 [ **advanced** ] 模式不是作用中，則在功能區 UI 中將不會顯示該 **群組** 以及其中的任何控制項（強制回應或其他）。

使用 *ApplicationModes* 屬性時，模式會指派給1： N (一對多) 關聯性中的強制回應控制項，其中單一模式控制項可以與數個模式相關聯。

功能區架構指的是數位的模式，從0到31，而模式0則是在功能區應用程式啟動時自動啟動的預設模式。 未指定 *ApplicationModes* 屬性的任何模式控制項都會被視為預設模式的成員。

在 RibbonApp 中， **Simple** 是預設模式，只有在使用者啟動時才會顯示 [ **Advanced** mode] 功能。

下列範例示範 RibbonApp 所需的標記。


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



此範例示範下列各項：

-   不需要明確宣告預設模式0。 因為未指定 *ApplicationModes* 屬性的強制回應控制項會自動系結至) RibbonApp 範例中的模式 0 (**簡單** 模式，所以不需要明確宣告預設強制回應控制項的屬性。
-   控制項可以系結至多個模式。 針對 RibbonApp，**簡單** 模式控制項中 *ApplicationModes* 屬性的唯一需求是 `cmdSwitchModes` 按鈕，因為它是 **簡單** 和 **先進** 模式的一部分。 如果其中一個模式為使用中，此控制項將會出現在 [ [應用程式] 功能表](windowsribbon-controls-applicationmenu.md)中。
-   強制回應控制項不會繼承自其父代。 RibbonApp 的 [ **Advanced** ] 索引標籤包含 **中繼資料** 群組;這兩個模式控制項都指派給模式 1 (**Advanced** 模式) 。 將 [ **Advanced** ] 索引標籤指派給模式1，並不會自動將子控制項（例如 **中繼資料** 群組）指派給模式1。 這可讓索引標籤內的任何群組在執行時間獨立啟用或停用。
-   非強制回應控制項仍然可以依賴模式切換。 RibbonApp 的 [ **編輯中繼資料** ] 和 [ **檢查錯誤** ] 按鈕是否適用于 advanced users，而且只有在使用者切換至 **advanced** 模式時才可使用。 未裝載在 [應用程式功能表](windowsribbon-controls-applicationmenu.md) 內的按鈕控制項為非強制回應;不過，由於這些按鈕是裝載在 (**中繼資料** 群組) 的強制回應控制項內，因此當群組為可見時，就會顯示這些按鈕。 因此，當啟動 advanced 模式並在功能區 UI 中公開 **中繼資料** 群組時，就會出現這些按鈕。

### <a name="switch-modes-at-runtime"></a>執行時間切換模式

在標記中定義模式之後，您可以輕鬆地啟用或停用這些模式，以回應內容相關事件。 如先前所述，功能區應用程式一律會以預設模式0開始。 在應用程式初始化且模式0為使用中之後，即可藉由呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) 函式來變更現用模式的集合。 此函式會採用32位整數作為應為作用中之模式的位標記法;最不重要的位代表模式0，而最大的位代表模式31。 如果位設定為零，則在功能區 UI 中不會使用此模式。

在 RibbonApp 中，當使用者啟用 **advanced** 模式時，Advanced 命令會與簡單的命令一起顯示。 **切換至 [切換至 Advanced 模式]** 按鈕的命令處理常式會呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) ，以將模式 0 (**簡單** 的) 和 1 (**Advanced**) 在 UI 中為作用中。 下列範例是此函式呼叫的 RibbonApp 程式碼：


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> 功能區架構 UI \_ MAKEAPPMODE 宏可簡化正確設定這些位的工作，以準備呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)。

 

此範例示範下列各項：

-   使用 UI \_ MAKEAPPMODE 宏來建立模式設定。
-   模式會以明確且明確的方式設定。 傳遞給 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) 的整數值代表在函式傳回之後將會作用的模式。 雖然 **簡單** 模式先前為使用中，但 **IUIFramework：： SetModes** 必須指出當啟動 **Advanced** 模式時，**簡單** 模式仍保持作用中狀態。
-   可以移除預設模式。 雖然在 RibbonApp 中，預設模式 (模式 0) 不會被移除，但您可以使用下列呼叫來移除它： `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` ，只會在 UI 中公開 advanced 命令。

> [!Note]  
> 重新設定應用程式的模式時，功能區會嘗試保留 UI 中先前選取的索引標籤。 如果新的一組模式不再包含呼叫之前選取的索引標籤，功能區將會在其配置中選取最接近 [應用程式功能表](windowsribbon-controls-applicationmenu.md)的索引標籤。 此索引標籤的目的是要包含與使用者最相關的命令。 如需詳細資訊，請參閱 [功能區使用者經驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)。

 

## <a name="remarks"></a>備註

功能區隨時都必須有一個主動模式。 如果應用程式透過呼叫 [**IUIFramework：： SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) （其模式值為0）來嘗試停用所有模式， \_ 則會傳回 E 失敗，而且主動模式設定會維持不變。

此架構要求功能區 UI 中必須至少有一個索引標籤存在。 如此一來，預設模式至少必須有一個索引標籤 (模式 0) 和每個模式切換之後。

功能區 UI 的所有區域都不會受到應用程式模式的影響。 例如，如果停用模式導致從先前新增至 [快速存取工具列](windowsribbon-controls-quickaccesstoolbar.md)的功能區消失按鈕，這些按鈕會保留在快速存取工具列中，讓使用者可以執行系結至按鈕的命令。 一般來說，如果某個命令屬於一或多個非使用中的模式，則該命令也應該停用，方法是將 [ [UI \_ PKEY \_ Enabled](windowsribbon-reference-properties-uipkey-enabled.md) ] 屬性設定為 0 (VARIANT \_ FALSE) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[功能區使用者體驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[顯示內容索引標籤](ribbon-contextualtabs.md)
</dt> </dl>

 

 