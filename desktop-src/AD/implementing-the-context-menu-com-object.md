---
title: 執行內容功能表 COM 物件
description: 內容功能表延伸是實作為同進程伺服器的 COM 物件。
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- 內容功能表 COM 物件廣告
- 內容功能表 COM 物件廣告，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac371ea64239c18de2a8f30c969eb6d920221f0a802f18ceeebfef2c3991e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187646"
---
# <a name="implementing-the-context-menu-com-object"></a>執行內容功能表 COM 物件

內容功能表延伸是實作為同進程伺服器的 COM 物件。 內容功能表延伸模組必須執行 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面。 當使用者顯示已註冊內容功能表延伸之類別物件的內容功能表時，會具現化內容功能表延伸。

## <a name="implementing-ishellextinit"></a>執行 IShellExtInit

在內容功能表延伸 COM 物件具現化之後，會呼叫 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 方法。 **IShellExtInit：： Initialize** 會提供內容功能表延伸，內含 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) 物件，其中包含與內容功能表適用的目錄物件相關的資料。

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)包含 [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format)格式的資料。 **CFSTR \_ DSOBJECTNAMES** 資料格式是包含 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)結構的 **HGLOBAL** 。 **DSOBJECTNAMES** 結構包含屬性工作表延伸適用之目錄物件的相關資料。

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)也包含 [**CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項**](cfstr-ds-display-spec-options.md)格式的資料。 **CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項** 資料格式是包含 [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)結構的 **HGLOBAL** 。 **DSDISPLAYSPECOPTIONS** 包含延伸模組所使用的設定資料。

如果從 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)傳回 **S \_ [確定]** 以外的任何值，將不會使用內容功能表延伸。

不會使用 [**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 *pidlFolder* 和 *hkeyProgID* 參數。

## <a name="implementing-icontextmenu"></a>執行 ICoNtextMenu

[**IShellExtInit：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)傳回之後，會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)方法來取得功能表項目，或是內容功能表延伸模組將加入的專案。 **QueryCoNtextMenu** 的執行相當簡單。 內容功能表延伸會使用 [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) 或類似的函式來加入其功能表項目。 功能表命令識別碼必須大於或等於 *idCmdFirst* ，而且必須小於 *idCmdLast*。 **QueryCoNtextMenu** 必須傳回已新增至功能表的最大數值識別碼，再加一。 指派功能表命令識別碼的最佳方式是從零開始，然後依序進行處理。 如果內容功能表延伸不需要任何功能表項目，則只應該將任何專案加入至功能表，並從 **QueryCoNtextMenu** 傳回零。

呼叫 [**ICoNtextMenu：： GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) ，以抓取功能表項目的文字資料，例如要針對功能表項目顯示的解說文字。 當擴充功能使用 ANSI 字串時，內容功能表主機可能會使用 Unicode 字串。 因此， **gc \_ HELPTEXTA**、 **gc \_ HELPTEXTW**、 **gc \_ VERBA** 和 **gc \_ VERBW** 案例必須個別處理。 這種方法的執行是選擇性的。

當選取內容功能表延伸模組所安裝的其中一個功能表項目時，就會呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 。 內容功能表會執行或起始所需的動作，以回應這個方法。

 

 