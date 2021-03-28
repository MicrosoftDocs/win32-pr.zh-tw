---
description: 將動詞新增至串聯功能表的另一個選項是透過 IExplorerCommand：： EnumSubCommands。
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: 使用 IExplorerCommand 介面建立串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104552866"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>如何使用 IExplorerCommand 介面建立串聯功能表

將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。 這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 介面提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。 在 Windows 7 （含）以後版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 介面來提供相同的動詞實行，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面一樣。

## <a name="instructions"></a>指示


以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/filecascademenu.png)

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a>備註

> [!Note]  
> 因為 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 僅支援同進程啟用，所以建議您在需要于命令和快捷方式功能表之間共用執行的 Shell 資料來源使用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
