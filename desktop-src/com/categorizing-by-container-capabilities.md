---
title: 依容器功能分類
description: 元件通常需要容器中的特定功能，且不會使用不提供支援的容器。
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67811a40c2c1bbffd4529b3f7c885a0d3e2bea19bda04035ffb80b601c266807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310885"
---
# <a name="categorizing-by-container-capabilities"></a>依容器功能分類

元件通常需要容器中的特定功能，且不會使用不提供支援的容器。 使用者介面應該篩選出需要容器不支援之功能的元件。 為了達成此目的，元件可以依必要的容器功能分類。

需要容器中的功能，但無法在不支援該功能的容器中運作的元件範例是簡單的框架 OLE 控制項。 依容器功能分類可透過元件的 CLSID 機碼中的額外登錄機碼來完成：

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

如這個範例所示，元件可以屬於表示支援之功能的元件類別，以及表示所需功能的元件類別。

在下列範例中，按鈕控制項是不支援其他功能的一般 OLE 控制項。 它可在任何 OLE 控制項容器中運作。

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

比較上述範例與下一個範例，如果容器支援，MyDBControl 可以使用 Visual Basic 資料系結。 不過，已定義它，使其可在不支援 Visual Basic 資料系結的容器中運作 (可能) 不同的資料庫 API：

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

群組方塊控制項是一個簡單的框架控制項。 它會依賴執行 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 介面的容器，而且只能在這類容器中正確運作：

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

支援 Visual Basic 資料繫結控制項，但不支援簡單框架控制項的容器，會指定 \_ \_ insert 控制項使用者介面的 catid 控制項和 catid VBDatabound。 顯示給使用者的控制項清單會包含 CLSID \_ 按鈕和 clsid \_ MyDBControl。 \_不會顯示 CLSID 的分組。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將圖示與類別產生關聯](associating-icons-with-a-category.md)
</dt> <dt>

[依元件功能分類](categorizing-by-component-capabilities.md)
</dt> <dt>

[預設類別和關聯](default-classes-and-associations.md)
</dt> <dt>

[定義元件類別](defining-component-categories.md)
</dt> <dt>

[元件類別管理員](the-component-categories-manager.md)
</dt> </dl>

 

 




