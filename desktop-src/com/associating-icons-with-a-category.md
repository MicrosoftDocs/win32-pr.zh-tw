---
title: 將圖示與類別產生關聯
description: 將圖示與類別產生關聯
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020975"
---
# <a name="associating-icons-with-a-category"></a>將圖示與類別產生關聯

建立使用者介面，讓使用者能夠選取類別內的元件類別目錄，需要能夠針對特定類別目錄顯示有意義的影像。 若要將圖示與元件類別建立關聯，請建立類別的 CATID 的金鑰，並使用 [DefaultIcon](defaulticon.md) 子機碼填入該金鑰。 登錄專案如下所示：

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

DefaultIcon 索引鍵所參考的檔案名可以是 EXE 或 DLL 檔案 (僅限資源的 DLL) 。

若要建立小型 16x16 "工具箱點陣圖與元件類別之間的關聯，請在類別的 CATID 的 **HKEY \_ 類別 \_ 根 \\ CLSID** 中建立索引鍵，並使用 [ToolBoxBitmap32](toolboxbitmap32.md) 子機碼填入該索引鍵，如下列範例所示：

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

[ToolBoxBitmap32](toolboxbitmap32.md)索引鍵所參考的檔案名也可以是 EXE 或 dll 檔案 (僅限資源的 DLL) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[依元件功能分類](categorizing-by-component-capabilities.md)
</dt> <dt>

[依容器功能分類](categorizing-by-container-capabilities.md)
</dt> <dt>

[預設類別和關聯](default-classes-and-associations.md)
</dt> <dt>

[定義元件類別](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[元件類別管理員](the-component-categories-manager.md)
</dt> </dl>

 

 




