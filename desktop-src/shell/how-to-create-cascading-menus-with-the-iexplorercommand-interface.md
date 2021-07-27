---
description: 將動詞新增至串聯功能表的另一個選項是透過 IExplorerCommand：： EnumSubCommands。
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: 使用 IExplorerCommand 介面建立串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436093"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>如何使用 IExplorerCommand 介面建立串聯功能表

將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。 這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 介面提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。 在 Windows 7 和更新版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)介面來提供相同的動詞實，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)介面一樣。

## <a name="instructions"></a>指示


以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/FileCascadeMenu.png)

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadeDevices2.png)

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

 

 
