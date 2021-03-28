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
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="aabaa-103">如何使用 IExplorerCommand 介面建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="aabaa-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="aabaa-104">將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。</span><span class="sxs-lookup"><span data-stu-id="aabaa-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="aabaa-105">這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 介面提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="aabaa-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="aabaa-106">在 Windows 7 （含）以後版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 介面來提供相同的動詞實行，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面一樣。</span><span class="sxs-lookup"><span data-stu-id="aabaa-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="aabaa-107">指示</span><span class="sxs-lookup"><span data-stu-id="aabaa-107">Instructions</span></span>


<span data-ttu-id="aabaa-108">以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="aabaa-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/filecascademenu.png)

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="aabaa-111">備註</span><span class="sxs-lookup"><span data-stu-id="aabaa-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aabaa-112">因為 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 僅支援同進程啟用，所以建議您在需要于命令和快捷方式功能表之間共用執行的 Shell 資料來源使用。</span><span class="sxs-lookup"><span data-stu-id="aabaa-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aabaa-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="aabaa-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aabaa-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="aabaa-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="aabaa-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="aabaa-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="aabaa-116">**ICoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="aabaa-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
