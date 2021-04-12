---
title: 使用值對應注釋
description: 如需範例程式碼，請參閱值對應注釋範例。
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375425"
---
# <a name="using-value-map-annotation"></a>使用值對應注釋

**若要建立值對應**

1.  **建立對應字串。**

    對應字串是控制項數值的清單，這些值會對應至 Unicode 中人們可讀取的字串。 開頭為 "A："，後面接著一個數位，指出所使用的索引類型。 僅支援影像索引;因此，索引類型一律為0。

    字串後面接著： index： result 配對。 「索引」是代表 List-View 或樹狀檢視之影像索引的數位，或是滑杆控制項的值。

    產生的值是當您對應清單視圖或樹狀檢視控制項的角色或狀態屬性時，所取得的數位。 這類數位會以十進位或十六進位以 "0x" 前置詞表示。

    對應字串一律以最後的冒號結束， ( "：" ) 。

    以下是清單視圖或樹狀檢視控制項中核取方塊的 [狀態] 和 [角色] 屬性的批註對應範例。 視圖中有兩個代表核取方塊的專案，而且每個專案都有對應至已核取和未核取狀態的影像。

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    如需有效的角色和狀態值，請參閱 [物件角色](object-roles.md) 和 [物件狀態常數](object-state-constants.md)。

    當您對應滑杆控制項的屬性時，索引值可能是負數。

    當您對應值或描述屬性時，結果會是字串。 字串不會加上引號，而冒號可作為分隔符號。

    如需詳細資訊，請參閱 [批註對應格式](value-map-annotation.md)。

2.  **建立注釋管理員，並取得其**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**介面** 的指標。

    以下是如何建立注釋管理員的範例。

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  **將對應字串附加至控制項。**

    呼叫 [**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)，將控制項的 **HWND** 和指標傳遞至對應字串。

    *IdProp* 參數將會是下列其中一項。

    

    | 參數                   | 用途                                                |
    |-----------------------------|---------------------------------------------------------|
    | MSAAPROPID \_ ROLEMAP         | 設定清單視圖或樹狀檢視控制項的角色對應。  |
    | MSAAPROPID \_ STATEMAP        | 設定清單視圖或樹狀檢視控制項的狀態對應。 |
    | PROPID \_ ACC \_ DESCRIPTIONMAP | 為清單視圖或樹狀檢視設定描述對應。   |
    | MSAAPROPID \_ VALUEMAP        | 設定滑杆控制項的值對應。                  |

    

     

4.  **清除。**

    在您終結任何值對應標注的控制項之前 (例如，處理 [WM \_ ](../winmsg/wm-destroy.md) 終結) 時，您必須清除先前註冊的屬性，並釋放注釋管理員。

    若要這樣做，請適當地呼叫 [**IAccPropServices：： ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) ，並釋放您的指標以進行 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)。

如需範例程式碼，請參閱 [值對應注釋範例](value-map-annotation-sample.md)。

 

 